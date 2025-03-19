# Mind2

This repository contains the official dataset and evaluations based on [ESC](https://github.com/thu-coai/Emotional-Support-Conversation) for the paper "Mind2: Mind-to-Mind Emotional Support System with Bidirectional Cognitive Discourse Analysis." Click [here](https://drive.google.com/drive/folders/1rMlUqppihEj0S-herRpHTC2irbaBn0Nf?usp=sharing) to download.

### Abstract
-------------
Emotional support (ES) systems alleviate users' mental distress by generating strategic supportive dialogues based on diverse user situations. However, ES systems are limited in their ability to generate effective ES dialogues that include timely context and interpretability, hindering them from earning public trust. Driven by cognitive models, we propose Mind-to-Mind (Mind2), an ES framework that approaches interpretable ES context modeling for the ES dialogue generation task from a discourse analysis perspective. Specifically, we perform cognitive discourse analysis on ES dialogues according to our dynamic discourse context propagation window, which accommodates evolving context as the conversation between the ES system and user progresses. To enhance interpretability, Mind2 prioritizes details that reflect each speaker's belief about the other speaker with bidirectionality, integrating Theory-of-Mind, physiological expected utility, and cognitive rationality to extract cognitive knowledge from ES conversations. Experimental results support that Mind2 achieves competitive performance versus state-of-the-art ES systems while trained with only 10% of the available training data. 

### Quick Start
----------------
Install [PyTorch](https://pytorch.org/) and required packages in ``requirements.txt``
```
pip install -r requirements.txt
```

### Data Processing
--------------------
```
python prepare.py --knowlege mind2 --train_input_file ./data/
```

### Training 
-------------
```
python train.py --knowledge_name mind2 --eval_input_file ./data/
```

### Evaluation
---------------
```
python infer.py --knowledge_name mind2 --add_nlg_eval --infer_input_file ./data/ --load_checkpoint {best_checkpoint_path}
```

### Citation
-------------
```
@inproceedings{hong-etal-2024-mind2,
  title={Mind2: Mind-to-Mind Emotional Support System with Bidirectional Cognitive Discourse Analysis},
  author={Hong, Shi Yin and 
    Oyshi, Uttamasha and 
    Mai, Quan and 
    Nkhata, Gibson and 
    Gauch, Susan},
  booktitle={IEEE/WIC International Conference on Web Intelligence and Intelligent Agent Technology},
  year={2024}
}
```
