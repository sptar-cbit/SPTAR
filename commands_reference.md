conda activate ~/miniconda3/envs/py37

python -m zhiyuan.retriever.bm25anserini.evaluate_anserini_bm25 --dataset_name fiqa

python train_sbert.py --dataset_name fiqa --train_num 50 --exp_name no_aug --weak_num 100k

 docker run -it --rm -e JAVA_OPTS="-Xmx8g" -p 8002:8000 beir/pyserini-fastapi
