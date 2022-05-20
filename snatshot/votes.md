```typescript
////////////            API            ////////////
const request_vote = fetch("https://hub.snapshot.org/graphql", {
  "headers": {
    "accept": "*/*",
    "accept-language": "zh-CN,zh;q=0.9,en-US;q=0.8,en;q=0.7,zh-TW;q=0.6",
    "content-type": "application/json",
    "sec-ch-ua": "\" Not A;Brand\";v=\"99\", \"Chromium\";v=\"101\", \"Google Chrome\";v=\"101\"",
    "sec-ch-ua-mobile": "?1",
    "sec-ch-ua-platform": "\"Android\"",
    "sec-fetch-dest": "empty",
    "sec-fetch-mode": "cors",
    "sec-fetch-site": "same-site"
  },
  "referrer": "https://snapshot.org/",
  "referrerPolicy": "strict-origin-when-cross-origin",
  "body": "{\"operationName\":\"Votes\",\"variables\":{\"id\":\"提案ID\",\"orderBy\":\"vp\",\"orderDirection\":\"desc\",\"first\":10},\"query\":\"query Votes($id: String!, $first: Int, $skip: Int, $orderBy: String, $orderDirection: OrderDirection, $voter: String) {\\n  votes(\\n    first: $first\\n    skip: $skip\\n    where: {proposal: $id, vp_gt: 0, voter: $voter}\\n    orderBy: $orderBy\\n    orderDirection: $orderDirection\\n  ) {\\n    ipfs\\n    voter\\n    choice\\n    vp\\n    vp_by_strategy\\n  }\\n}\"}",
  "method": "POST",
  "mode": "cors",
  "credentials": "omit"
});

const respond_vote = {
  "data": {
    "votes": [
      {
        "ipfs": "QmcZg9CRTCToBVfTMkRsFfH4bRWAqUorp9h1YUNUSMvsfr",
        "voter": "投票者地址",
        "choice": 1,  //   投票表态
        "vp": 325053.57791152014, //   投票权重
        "vp_by_strategy": [
          0,
          325053.57791152014
        ]
      },
    ]
  }
}

////////////            Example            ////////////

const request_vote_1 = fetch("https://hub.snapshot.org/graphql", {
  "headers": {
    "accept": "*/*",
    "accept-language": "zh-CN,zh;q=0.9,en-US;q=0.8,en;q=0.7,zh-TW;q=0.6",
    "content-type": "application/json",
    "sec-ch-ua": "\" Not A;Brand\";v=\"99\", \"Chromium\";v=\"101\", \"Google Chrome\";v=\"101\"",
    "sec-ch-ua-mobile": "?1",
    "sec-ch-ua-platform": "\"Android\"",
    "sec-fetch-dest": "empty",
    "sec-fetch-mode": "cors",
    "sec-fetch-site": "same-site"
  },
  "referrer": "https://snapshot.org/",
  "referrerPolicy": "strict-origin-when-cross-origin",
  "body": "{\"operationName\":\"Votes\",\"variables\":{\"id\":\"0x718c496b04017fb82749b68570d12f32c839f59b9f9433df127f48bf99121eb7\",\"orderBy\":\"vp\",\"orderDirection\":\"desc\",\"first\":10},\"query\":\"query Votes($id: String!, $first: Int, $skip: Int, $orderBy: String, $orderDirection: OrderDirection, $voter: String) {\\n  votes(\\n    first: $first\\n    skip: $skip\\n    where: {proposal: $id, vp_gt: 0, voter: $voter}\\n    orderBy: $orderBy\\n    orderDirection: $orderDirection\\n  ) {\\n    ipfs\\n    voter\\n    choice\\n    vp\\n    vp_by_strategy\\n  }\\n}\"}",
  "method": "POST",
  "mode": "cors",
  "credentials": "omit"
});

const respond_vote_1 = {
  "data": {
    "votes": [
      {
        "ipfs": "QmcZg9CRTCToBVfTMkRsFfH4bRWAqUorp9h1YUNUSMvsfr",
        "voter": "0x983110309620D911731Ac0932219af06091b6744",
        "choice": 1,
        "vp": 325053.57791152014,
        "vp_by_strategy": [
          0,
          325053.57791152014
        ]
      },
      {
        "ipfs": "QmYGmz39UriRDTsyYc25ciM4T4xXdKKu8WeaiUrK3YM6HX",
        "voter": "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
        "choice": 1,
        "vp": 232446.48478982778,
        "vp_by_strategy": [
          0,
          232446.48478982775
        ]
      },
      {
        "ipfs": "QmZAwjfcnTfSzrivQyBKhLfaL9xoy7JKfBJ1fqn85LEhmi",
        "voter": "0x2B888954421b424C5D3D9Ce9bB67c9bD47537d12",
        "choice": 1,
        "vp": 207977.9886071505,
        "vp_by_strategy": [
          0,
          207977.9886071505
        ]
      },
      {
        "ipfs": "QmTPQ72P9tqW3RGF3dzYNuyvjcKH3H2uZJpFg8uD1wcKaz",
        "voter": "0x399e0Ae23663F27181Ebb4e66Ec504b3AAB25541",
        "choice": 1,
        "vp": 135405.72252659785,
        "vp_by_strategy": [
          0,
          135405.72252659785
        ]
      },
      {
        "ipfs": "QmckaNxRwQMBsmeAz8B1eUjn1KY4FdxQVVXBKGWvFb31Lh",
        "voter": "0x3B3525F60eeea4a1eF554df5425912c2a532875D",
        "choice": 1,
        "vp": 113639.90542960729,
        "vp_by_strategy": [
          0,
          113639.90542960729
        ]
      },
      {
        "ipfs": "QmT2PdgE9N3zuAxb1jKxVHkiDDn6uKFRkpsEqogS7aBPL3",
        "voter": "0x904bC15358C40Ba6C1e45F10e65d052001e9eDd2",
        "choice": 1,
        "vp": 87416.67611172874,
        "vp_by_strategy": [
          87416.67611172874,
          0
        ]
      },
      {
        "ipfs": "QmUcHuT1TTCRh3TMHASgc7GWj11i7EqqUrYkZ6iJSmJuVo",
        "voter": "0x8b3347FD0B8C3a619d1f1FDc90CAF4F335c03742",
        "choice": 1,
        "vp": 60016.255643033575,
        "vp_by_strategy": [
          0,
          60016.255643033575
        ]
      },
      {
        "ipfs": "QmaPrXxd8BF4zwczgVNLhZ8WHmWtqmUFbFKvioKMxSWV3f",
        "voter": "0x9B6568d72A6f6269049Fac3998d1fadf1E6263cc",
        "choice": 1,
        "vp": 59640.37341318469,
        "vp_by_strategy": [
          59640.37341318469,
          0
        ]
      },
      {
        "ipfs": "QmQpbfNy1SpfUuSyRmYgcFRRUc2EzrUo8iEBiapqobr6Ua",
        "voter": "0x48dbB9B7B562ACf3c38E53deAfF4686e24c3D85D",
        "choice": 1,
        "vp": 58461.49263343038,
        "vp_by_strategy": [
          0,
          58461.49263343038
        ]
      },
      {
        "ipfs": "QmbjCUHL1xTiDGj7EYqot2ThbbsbVyreGXEEBoB92zRygG",
        "voter": "0x534631Bcf33BDb069fB20A93d2fdb9e4D4dD42CF",
        "choice": 1,
        "vp": 56237.61880645607,
        "vp_by_strategy": [
          0,
          56237.61880645607
        ]
      }
    ]
  }
}
```
