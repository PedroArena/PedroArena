var myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");

var raw = JSON.stringify({
  "id": 67,
  "jsonrpc": "2.0",
  "method": "qn_fetchNFTsByCollection",
  "params": [{
    "collection": "0x60E4d786628Fea6478F785A6d7e704777c86a7c6",
    "omitFields": [
      "imageUrl",
      "traits"
    ],
    "page": 1,
    "perPage": 10
  }]
});

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: raw,
  redirect: 'follow'
};

fetch("http://sample-endpoint-name.network.quiknode.pro/token-goes-here/", requestOptions)
  .then(response => response.text())
  .then(result => console.log(result))
  .catch(error => console.log('error', error));

