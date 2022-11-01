# NextParagraphPrediction
Next Paragraph Prediction model and Reddit datasets (original and instructional prompts versions)


Library Requirement (on CoLab)
torchtext==0.8.0 torch==1.7.1 pytorch-lightning==1.2.2
transformers==3.4

In nsp folder:
training.py is preset for fine-tuning with RoBerta Large model.
training-base.py is preset for fine-tuning with RoBerta Base model.
trainingBERT.py is preset for fine-tuning with BERT Large model.
trainingBERT-base.py is preset for fine-tuning with BERT Base model.


To Train Model: Fine-Tune with RoBerta Large model and instructional prompts Reddit dataset.
python training.py ../Prompt-reddit/RedditNewTrain.csv ../Prompt-reddit/RedditNewDev.csv

To Evaluate the fine-tuned model: (Evaluate with epoch 0 checkpoint model)
python validation.py lightning_logs/version_0/checkpoints/epoch\=0-step\=1225.ckpt ../Prompt-reddit/RedditNewTest.csv
