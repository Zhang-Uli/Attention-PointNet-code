# Attention-PointNet-code
  Code Execution Guidelines for "Identification and analysis of rock mass discontinuities based on Attention-PointNet++ using forward modeling training datasets"
The following are the standardized steps for running the code associated with the paper:
1. Configure Training Parameters in the Core Script
  Open the "train_partseg.py" file and adjust key parameters based on actual segmentation tasks:
(1) Modify seg_class, num_class, and num_cart to match the specific requirements of your segmentation task.
(2) Optimize hyperparameters such as '--batch_size', '--epoch', '--npoint', and num_workers according to your hardware performance and dataset scale. 
2. Prepare and Deploy the Dataset.
  Place your custom dataset in the root directory 'data/Canada_data/'. The dataset should be preprocessed to support the construction of training and validation sets.
3. Select the Appropriate Model Architecture
  Continue configuring the "train_partseg.py" file and specify the '--model' parameter based on whether the self-attention mechanism is required:
(1) Choose 'pointnet2_part_seg_msg' if the self-attention mechanism is not needed.
(2) Select 'pointnet2_part_seg_msg_attention' to enable the self-attention mechanism.
4. Initiate Model Training
  Run the configured "train_partseg.py" file to start the network training process. Monitor training metrics in real time to adjust parameters dynamically if necessary, ensuring the model converges effectively.
5. Perform Testing and Export Results
  After training is completed, use the "test_partseg.py" file for recognition testing. Modify relevant parameters, consistent with the training configuration and specify the file_path according to actual needs to export the recognition results to the target location for subsequent analysis and verification.
