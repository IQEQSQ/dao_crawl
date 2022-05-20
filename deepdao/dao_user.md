
```typescript

////////////            API            ////////////    
const request_dao_user = fetch("https://golden-gate-server.deepdao.io/user/2/钱包地址", {
  "headers": {
    "accept": "application/json, text/plain, */*",
    "accept-language": "zh-CN,zh;q=0.9,en-US;q=0.8,en;q=0.7,zh-TW;q=0.6",
    "if-none-match": "W/\"2bc-SLh9DGs+jxiBCSBcQFdLJtwlSNk\"",
    "sec-ch-ua": "\" Not A;Brand\";v=\"99\", \"Chromium\";v=\"101\", \"Google Chrome\";v=\"101\"",
    "sec-ch-ua-mobile": "?1",
    "sec-ch-ua-platform": "\"Android\"",
    "sec-fetch-dest": "empty",
    "sec-fetch-mode": "cors",
    "sec-fetch-site": "same-site"
  },
  "referrer": "https://deepdao.io/",
  "referrerPolicy": "strict-origin-when-cross-origin",
  "body": null,
  "method": "GET",
  "mode": "cors",
  "credentials": "omit"
});
const respond_dao_user = {
  "address": "钱包地址",
  "name": "名字",
  "github": "github地址",
  "twitter": "推特",
  "website": "个人网站",
  "aum": null,
  "totalAum": null,
  "createdAt": null,
  "description": "个人描述",
  "avatar": "",
  "personalInfo": {},
  "totalDaos": 1,   //  拥有的Dao数量
  "totalOrgs": 1,   //  所在的组织数量
  "totalProposals": 0,  //  有多少次提案
  "totalVotes": 0, //  有多少次投票
  "participationScore": 0.1,    //  治理参与积分
  "relativeScore": 0.0555247084952839, //  治理参与相对积分
  "participationScoreRank": 1800, //  治理参与排名
  "daos": [//  加入的Dao的组织的相信信息
    {
      "daoId": "4137cd30-33fa-42bc-8395-5aa8920005f5",
      "organizationId": "60c9b31c-4495-4028-aeac-eb7bb117fece",
      "name": "Decentraland",
      "address": "0x9A6ebE7E2a7722F8200d0ffB63a1F6406A0d7dce",
      "image": "https://deepdao-uploads.s3.us-east-2.amazonaws.com/assets/snapshots/spaces/snapshot.dcl.eth.png",
      "membersAmount": null,
      "proposalsAmount": null
    }
  ],
  "tokens": []
}


////////////            Example            ////////////    

const request_dao_user_1 = fetch("https://golden-gate-server.deepdao.io/user/2/0xefb94ac00f1cee8a89d5c3f49faa799da6f03024", {
  "headers": {
    "accept": "application/json, text/plain, */*",
    "accept-language": "zh-CN,zh;q=0.9,en-US;q=0.8,en;q=0.7,zh-TW;q=0.6",
    "if-none-match": "W/\"2bc-SLh9DGs+jxiBCSBcQFdLJtwlSNk\"",
    "sec-ch-ua": "\" Not A;Brand\";v=\"99\", \"Chromium\";v=\"101\", \"Google Chrome\";v=\"101\"",
    "sec-ch-ua-mobile": "?1",
    "sec-ch-ua-platform": "\"Android\"",
    "sec-fetch-dest": "empty",
    "sec-fetch-mode": "cors",
    "sec-fetch-site": "same-site"
  },
  "referrer": "https://deepdao.io/",
  "referrerPolicy": "strict-origin-when-cross-origin",
  "body": null,
  "method": "GET",
  "mode": "cors",
  "credentials": "omit"
});
const respond_dao_user_1 = {
  "address": "0xefb94ac00f1cee8a89d5c3f49faa799da6f03024",
  "name": "",
  "github": "",
  "twitter": "",
  "website": "",
  "aum": null,
  "totalAum": null,
  "createdAt": null,
  "description": "",
  "avatar": "",
  "personalInfo": {},
  "totalDaos": 1,
  "totalOrgs": 1,
  "totalProposals": 0,
  "totalVotes": 0,
  "participationScore": 0.1,
  "relativeScore": 0.0555247084952839,
  "participationScoreRank": 1800,
  "daos": [
    {
      "daoId": "4137cd30-33fa-42bc-8395-5aa8920005f5",
      "organizationId": "60c9b31c-4495-4028-aeac-eb7bb117fece",
      "name": "Decentraland",
      "address": "0x9A6ebE7E2a7722F8200d0ffB63a1F6406A0d7dce",
      "image": "https://deepdao-uploads.s3.us-east-2.amazonaws.com/assets/snapshots/spaces/snapshot.dcl.eth.png",
      "membersAmount": null,
      "proposalsAmount": null
    }
  ],
  "tokens": []
}

```
