# fastaionsagemaker

A AWS Cloudformation template to create an Amazon SageMaker instance with the fastai 0.7.x library for course.fast.ai.

### Notebook Instance Type

You can choose t2 instances for testing or choose ml.p2.xlarge or ml.p3.2xlarge if you wish to use an instance with a GPU, which is useful given we will train our fast.ai models on the same notebook instance. The ml.p2.xlarge instance has a Nvidia K80 GPU and the ml.p3.2xlarge has the more powerful Nvidia V100 GPU so training times for our models will be accelerated compared to other instance types. The ml.p3.2xlarge has a higher per hour charge than the ml.p2.xlarge ($4.284 vs $1.26 per hour in the N. Virginia Region), but you will most likely be able to train your deep learning models faster so the actual cost of training your model may be lower as you do not need to run the instance as long. The default limit per account of ml.p2.xlarge instances is 1 and for the ml.p3.2xlarge instances it is 2, so ensure that there are not too many other notebooks of the same type running in the same account to avoid hitting this limit or create a support case with AWS Support to request to have the limit increased. Details of the Amazon SageMaker default limits per account can be found here: https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html#limits_sagemaker.
