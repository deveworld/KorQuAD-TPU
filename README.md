# Table of contents
1. [KorQuAD-TPU](#korquad-tpu)
    1. [Notice](#notice)
2. [Usage](#usage)

# KorQuAD-TPU
A KorQuAD QuestionAnswering model training on TPU.

## Notice
This repository made by middle school student without a major.

In any case, I recommend that you DO NOT ATTEMPT training with this code.

# Usage

(I don't recommend training this, but) You will want to have TPU.

In my case, I got TPU v3-8 at [TPU Research Cloud](https://sites.research.google/trc/) for other research purpose.
And I had some resources to spare, so I worked on this project, alone.

If you really want to train this, get tpu at trc like me or pay for it at gcp.

If you have a tensorflow tpu vm(it's really important, use vm not node), clone this repo and run following code.

`python3 run_qa.py --model_name_or_path distilbert-base-cased-distilled-squad --output_dir OUTPUTDISK --dataset_name squad_kor_v2 --do_train --do_eval --tpu_name local --preprocessing_num_workers 10`

OUTPUTDISK must be a mounted disk from gcp compute disk.
