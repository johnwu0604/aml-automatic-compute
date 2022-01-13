# [Private Preview] Azure ML Automatic Compute

Automatic compute is a private preview feature in Azure ML that enables the submission of training jobs without having to create a compute target. Users can specify their compute requirements directly at job submission time and Azure ML will scale-up/scale-down the appropriate resources required for running the job. This feature is only available in the Studio UI during private preview. CLI and SDK support will be added at public preview.

To join the private preview, please fill out this [form](#).


## How to use the feature

For your convenience, this repository includes a training script that can be used as a sample to run the job. Steps `4-5` are defaulted to use the provided training script. If using a customized script, make sure to fill out the parameters accordingly based on your scenario.

1. Navigate to the [Azure ML Studio UI](https://master.ml.azure.com/?wsid=/subscriptions/4aaa645c-5ae2-4ae9-a17a-84b9023bc56a/resourceGroups/john/providers/Microsoft.MachineLearningServices/workspaces/john-west&flight=ClusterlessCompute,clusterlessComputeRun&tid=72f988bf-86f1-41af-91ab-2d7cd011db47).

2. From the top left corner, click on `+ New` and then followed by `Job (preview)`.

3. Make sure that `Automatic (preview)` is selected as the compute type. Then select your compute requirements and click `Next`.

4. Select the `TensorFlow 2.4` environment and click `Next`

5. Upload the `train.py` file, enter `python train.py` as the start command, and click `Next`.

6. Review your settings and click `Create`

7. Wait for the job to prepare. This may take a couple minutes if a job has not been submitted for awhile.

8. Once the job starts, you should be able to see metrics, logs, and monitoring information like with any other Azure ML job!

## How to submit feedback

To submit feedback, please use the built-in feedback tool in the Azure ML Studio UI.