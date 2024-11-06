```etcd
docker build -t etcd-local ./etcd
```

```etcd
docker run -d --name etcd-local -p 2379:2379 etcd-local
```
------------------------------------------------------------------------

```minio
docker build -t minio-local ./minio
```

```minio
docker run -d --name minio-local -p 9000:9000 -p 9001:9001 minio-local
```
------------------------------------------------------------------------

```milvus
docker build -t milvus-local ./milvus
```

```milvus
docker run -d --name milvus-local -p 19530:19530 -p 9091:9091 \
--link etcd-local:etcd \
--link minio-local:minio \
-e ETCD_ENDPOINTS=http://etcd:2379 \
-e MINIO_ADDRESS=minio:9000 \
-e MINIO_ACCESS_KEY=minioadmin \
-e MINIO_SECRET_KEY=minioadmin \
milvus-local
```

```milvus
docker run -d --name milvus-local -p 19530:19530 -p 9091:9091 \
--link etcd-local:etcd \
--link minio-local:minio \
milvus-local
```
------------------------------------------------------------------------

``` attu
docker build -t attu-local ./attu
```

``` attu
docker run -d --name attu-local -p 8000:3000 \
--link milvus-local:milvus \
-e MILVUS_URL=http://milvus:19530 \
attu-local
```

