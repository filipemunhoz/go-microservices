# go-microservices

## Introdution

Welcome! 👋

This is microservices written in ***go***.

This content was based on this [tutorial](https://www.youtube.com/watch?v=VzBGi_n65iU&ab_channel=NicJackson)

## SWAGGER - Docs
```
make
```

## SWAGGER - Generate Client
```
swagger generate client -f ../swagger.yaml -A go-microservices
```



## GET
```
curl  -v  -XGET localhost:8000/products | jq
```

## POST
```
curl -v localhost:8000/products -XPOST -H "Content-Type: application/json" -d '{"name":"Tea", "sku":"aaa-bbb-eee", "description":"I love tea", "price": 1.35}'
```

## PUT
```
curl -v localhost:8000/products/1 -XPOST -H "Content-Type: application/json" -d '{"name":"Tea", "sku":"aaa-bbb-eee", "description":"I love tea", "price": 2.74}'
```

## DELETE
```
curl -v localhost:8000/products/1 -XDELETE
```

## Uploading 

Note: need to use `--data-binary` to ensure file is not converted to text

```
curl -vv localhost:9090/1/go.mod -X PUT --data-binary @test.png
```
