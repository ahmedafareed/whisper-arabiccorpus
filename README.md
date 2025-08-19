# Whisper Small Arabic

This model is a fine-tuned version of [openai/whisper-small](https://huggingface.co/openai/whisper-small) on the Arabic News Corpus dataset.
It achieves the following results on the evaluation set:
- Loss: 0.2024
- 
## Training procedure

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 1e-05
- train_batch_size: 16
- eval_batch_size: 8
- seed: 42
- gradient_accumulation_steps: 2
- total_train_batch_size: 32
- optimizer: Use adamw_torch with betas=(0.9,0.999) and epsilon=1e-08 and optimizer_args=No additional optimizer arguments
- lr_scheduler_type: linear
- lr_scheduler_warmup_steps: 500
- training_steps: 1000
- mixed_precision_training: Native AMP
