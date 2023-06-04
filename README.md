curl http://sample-endpoint-name.network.quiknode.pro/token-goes-here/ \
  -X POST \
  -H "Content-Type: application/json" \
  -H "x-qn-api-version: 1" \
  --data '{
    "id":67,
    "jsonrpc":"2.0",
    "method":"qn_getTokenMetadataByContractAddress",
    "params":{
      "contract": "0x4d224452801ACEd8B2F0aebE155379bb5D594381"
    }
  }'
