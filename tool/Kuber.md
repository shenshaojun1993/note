# Kuber
kubectl port-forward --namespace ben-cces wistful-sloth-eric-aat-cces-jcat-7768b7d98c-pkwfx  9200:9200 &
kubectl get pods



kubectl get pods --namespace egugguo -l "app=eric-data-search-engine,role=ingest" -o jsonpath="{.items[0].metadata.name}"

pod=eric-data-search-engine-ingest-6cc9d7667d-l78v8

./start_elastic.sh egugguo

name=egugguo

eric-data-search-engine

kubectl port-forward --namespace egugguo eric-data-search-engine-ingest-6cc9d7667d-l78v8 9200:9200 &

remove INDEX