```typescript
////////////            API            ////////////
const request_dao_dao_info = fetch("https://hub.snapshot.org/graphql", {
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
  "body": "{\"operationName\":\"Spaces\",\"variables\":{\"id_in\":[\"DAO合约ID\",null]},\"query\":\"query Spaces($id_in: [String]) {\\n  spaces(where: {id_in: $id_in}) {\\n    id\\n    name\\n    about\\n    network\\n    symbol\\n    network\\n    terms\\n    skin\\n    avatar\\n    twitter\\n    website\\n    github\\n    private\\n    domain\\n    members\\n    admins\\n    categories\\n    plugins\\n    followersCount\\n    voting {\\n      delay\\n      period\\n      type\\n      quorum\\n      hideAbstain\\n    }\\n    strategies {\\n      name\\n      network\\n      params\\n    }\\n    validation {\\n      name\\n      params\\n    }\\n    filters {\\n      minScore\\n      onlyMembers\\n    }\\n  }\\n}\"}",
  "method": "POST",
  "mode": "cors",
  "credentials": "omit"
});

const respond_dao_info = {
  "data": {
    "spaces": [
      {
        "id": "ens.eth",    //  DAO合约ID
        "name": "ENS",    //  DAO名字
        "about": "",    //  关于这个DAO
        "network": "1",    // 这个DAO所在网络
        "symbol": "ENS",    // 这个DAO的治理代币
        "terms": null,
        "skin": null,
        "avatar": "ipfs://QmSL2X1h1uk26ahSALTw2qKyc61VaySRRstueVMm1Aym3e",
        "twitter": "ensdomains",    // 这个DAO的推特ID
        "website": null,   // 这个DAO的网址
        "github": "ensdomains",   // 这个DAO的Github信息
        "private": false,
        "domain": "ens.domains",   // 这个DAO的域名
        "members": [ // 这个DAO的部分成员列表
          "0x5A384227B65FA093DEC03Ec34e111Db80A040615",
          "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
          "0x983110309620D911731Ac0932219af06091b6744",
          "0x866B3c4994e1416B7C738B9818b31dC246b95eEE",
          "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
          "0x9297A132AF2A1481441AB8dc1Ce6e243d879eaFD",
          "0x75cac0CEb8A39DdB4942A83AD2aAfaF0C2A3e13f"
        ],
        "admins": [ // 这个DAO的管理员列表
          "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
          "0xb6E040C9ECAaE172a89bD561c5F73e1C48d28cd9",
          "0x75cac0ceb8a39ddb4942a83ad2aafaf0c2a3e13f",
          "0x9297A132AF2A1481441AB8dc1Ce6e243d879eaFD",
          "0x75cac0CEb8A39DdB4942A83AD2aAfaF0C2A3e13f"
        ],
        "categories": [], // 这个DAO的所属分类
        "plugins": {},
        "followersCount": 54957, // 这个DAO的成员数量
        "voting": {
          "delay": null,
          "period": 432000,
          "type": null,
          "quorum": null,
          "hideAbstain": false
        },
        "strategies": [
          {
            "name": "delegation",
            "network": "1",
            "params": {
              "symbol": "ENS (delegated)",
              "strategies": [
                {
                  "name": "erc20-votes",
                  "params": {
                    "symbol": "ENS",
                    "address": "0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72",
                    "decimals": 18
                  }
                }
              ]
            }
          },
          {
            "name": "erc20-votes",
            "network": "1",
            "params": {
              "symbol": "ENS",
              "address": "0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72",
              "decimals": 18
            }
          }
        ],
        "validation": {
          "name": "basic",
          "params": {}
        },
        "filters": {
          "minScore": 10000,
          "onlyMembers": false
        }
      }
    ]
  }
}

////////////            Example            ////////////

const request_dao_dao_info_1 = fetch("https://data.daohaus.club/dao/dao_infos", {
    headers: {
        accept: "*/*",
        "accept-language": "zh-CN,zh;q=0.9,en-US;q=0.8,en;q=0.7,zh-TW;q=0.6",
        "content-type": "text/plain;charset=UTF-8",
        "sec-ch-ua":
            '" Not A;Brand";v="99", "Chromium";v="101", "Google Chrome";v="101"',
        "sec-ch-ua-mobile": "?1",
        "sec-ch-ua-platform": '"Android"',
        "sec-fetch-dest": "empty",
        "sec-fetch-mode": "cors",
        "sec-fetch-site": "same-site",
    },
    referrer: "https://app.daohaus.club/",
    referrerPolicy: "strict-origin-when-cross-origin",
    body: '{"network":"xdai","minions":["0x04639d737c4ec157e99796778fe2596276e86851","0x16852e46732def952802f34b598370015a1fa054","0x3cea440fb5be559d4c1218b2c3ed74dc973147ad","0x6181d7c7d3256068cd11b95c811ec23edbb39731","0xb50a189d92306c0df61ef9d020be0ea14250316d","0xb8eb2970ab83d0dabce3406dde440daf98349cb3"]}',
    method: "POST",
    mode: "cors",
    credentials: "omit",
});

const respond_dao_dao_info_1 = {
  "data": {
    "spaces": [
      {
        "id": "ens.eth",
        "name": "ENS",
        "about": "",
        "network": "1",
        "symbol": "ENS",
        "terms": null,
        "skin": null,
        "avatar": "ipfs://QmSL2X1h1uk26ahSALTw2qKyc61VaySRRstueVMm1Aym3e",
        "twitter": "ensdomains",
        "website": null,
        "github": "ensdomains",
        "private": false,
        "domain": "ens.domains",
        "members": [
          "0x5A384227B65FA093DEC03Ec34e111Db80A040615",
          "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
          "0x983110309620D911731Ac0932219af06091b6744",
          "0x866B3c4994e1416B7C738B9818b31dC246b95eEE",
          "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
          "0x9297A132AF2A1481441AB8dc1Ce6e243d879eaFD",
          "0x75cac0CEb8A39DdB4942A83AD2aAfaF0C2A3e13f"
        ],
        "admins": [
          "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
          "0xb6E040C9ECAaE172a89bD561c5F73e1C48d28cd9",
          "0x75cac0ceb8a39ddb4942a83ad2aafaf0c2a3e13f",
          "0x9297A132AF2A1481441AB8dc1Ce6e243d879eaFD",
          "0x75cac0CEb8A39DdB4942A83AD2aAfaF0C2A3e13f"
        ],
        "categories": [],
        "plugins": {},
        "followersCount": 54957,
        "voting": {
          "delay": null,
          "period": 432000,
          "type": null,
          "quorum": null,
          "hideAbstain": false
        },
        "strategies": [
          {
            "name": "delegation",
            "network": "1",
            "params": {
              "symbol": "ENS (delegated)",
              "strategies": [
                {
                  "name": "erc20-votes",
                  "params": {
                    "symbol": "ENS",
                    "address": "0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72",
                    "decimals": 18
                  }
                }
              ]
            }
          },
          {
            "name": "erc20-votes",
            "network": "1",
            "params": {
              "symbol": "ENS",
              "address": "0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72",
              "decimals": 18
            }
          }
        ],
        "validation": {
          "name": "basic",
          "params": {}
        },
        "filters": {
          "minScore": 10000,
          "onlyMembers": false
        }
      }
    ]
  }
}
```
