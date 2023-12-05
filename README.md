# ClipCov subsets and Baseline Subsets

Baseline Subsets are in baseline_subsets/. 

ClipCov subsets are in clip_cov_subsets/. 

# Create Subset

The code for creating the subset is provided in clip_core.ipynb.

Due to size constraints we cannot upload the computed cosine similarity files etc. 

# Training Code

We train these subsets using the code provided by https://github.com/goel-shashank/CyCLIP.

The command we use to train the model is the following:

python -m src.main --name "<name_of_run>" --train_data <path_to_dataset_file> --image_key file --epochs 30 --batch_size 512 --distributed --device_ids <gpu_id_0> <gpu_id_1>

# Bibliography

@misc{goel2022cyclip,
      title={CyCLIP: Cyclic Contrastive Language-Image Pretraining}, 
      author={Shashank Goel and Hritik Bansal and Sumit Bhatia and Ryan A. Rossi and Vishwa Vinay and Aditya Grover},
      year={2022},
      eprint={2205.14459},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}