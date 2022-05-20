```typescript
////////////            API            ////////////
const request_proposals = fetch("https://hub.snapshot.org/graphql", {
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
  "body": "{\"operationName\":\"Proposals\",\"variables\":{\"first\":6,\"skip\":0,\"space\":\"DAO合约地址\",\"state\":\"all\",\"author_in\":[]},\"query\":\"query Proposals($first: Int!, $skip: Int!, $state: String!, $space: String, $space_in: [String], $author_in: [String]) {\\n  proposals(\\n    first: $first\\n    skip: $skip\\n    where: {space: $space, state: $state, space_in: $space_in, author_in: $author_in}\\n  ) {\\n    id\\n    ipfs\\n    title\\n    body\\n    start\\n    end\\n    state\\n    author\\n    created\\n    choices\\n    space {\\n      id\\n      name\\n      members\\n      avatar\\n      symbol\\n    }\\n    scores_state\\n    scores_total\\n    scores\\n    votes\\n    quorum\\n    symbol\\n  }\\n}\"}",
  "method": "POST",
  "mode": "cors",
  "credentials": "omit"
});

const respond_proposals = {
    "data": {
    "proposals": [
      {
        "id": "提案ID",
        "ipfs": "QmVgajsKijB9pjE7upTqgvNtwGyfnz8Sjm6ewwi4JXwvfS",
        "title": "提案标题",
        "body": "提案内容HTML",
        "start": 1650489821,    //  提案开始时间戳
        "end": 1650921821,    //  提案开始时间戳
        "state": "closed",    //  提案当前状态
        "author": "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",//   提案作者的钱包地址
        "created": 1650489827,   //  提案创建时间戳
        "choices": [ //  提案选项列表
          "For",
          "Against",
          "Abstain"
        ],
        "space": {
          "id": "ens.eth",   //  提案所属Dao组织
          "name": "ENS",   //  提案所属Dao组织的名字
          "members": [ //  提案所属Dao组织的管理员列表
            "0x5A384227B65FA093DEC03Ec34e111Db80A040615",
            "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
            "0x983110309620D911731Ac0932219af06091b6744",
            "0x866B3c4994e1416B7C738B9818b31dC246b95eEE",
            "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
            "0x9297A132AF2A1481441AB8dc1Ce6e243d879eaFD",
            "0x75cac0CEb8A39DdB4942A83AD2aAfaF0C2A3e13f"
          ],
          "avatar": "ipfs://QmSL2X1h1uk26ahSALTw2qKyc61VaySRRstueVMm1Aym3e",
          "symbol": "ENS"//  提案所属Dao组织的代币
        },
        "scores_state": "final",
        "scores_total": 1683490.2949245246,//  提案全部结果
        "scores": [
          1671001.3808671176,//  提案赞成结果
          12288.70648686089,//  提案反对结果
          200.20757054624133//  提案弃权结果
        ],
        "votes": 827,//  提案投票人数
        "quorum": 0,
        "symbol": "ENS"//  提案投票代币
      }
    ]
}

////////////            Example            ////////////

const request_proposals_1 = fetch("https://hub.snapshot.org/graphql", {
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
  "body": "{\"operationName\":\"Proposals\",\"variables\":{\"first\":6,\"skip\":0,\"space\":\"ens.eth\",\"state\":\"all\",\"author_in\":[]},\"query\":\"query Proposals($first: Int!, $skip: Int!, $state: String!, $space: String, $space_in: [String], $author_in: [String]) {\\n  proposals(\\n    first: $first\\n    skip: $skip\\n    where: {space: $space, state: $state, space_in: $space_in, author_in: $author_in}\\n  ) {\\n    id\\n    ipfs\\n    title\\n    body\\n    start\\n    end\\n    state\\n    author\\n    created\\n    choices\\n    space {\\n      id\\n      name\\n      members\\n      avatar\\n      symbol\\n    }\\n    scores_state\\n    scores_total\\n    scores\\n    votes\\n    quorum\\n    symbol\\n  }\\n}\"}",
  "method": "POST",
  "mode": "cors",
  "credentials": "omit"
});

const respond_proposals_1 = {
  "data": {
    "proposals": [
      {
        "id": "0x718c496b04017fb82749b68570d12f32c839f59b9f9433df127f48bf99121eb7",
        "ipfs": "QmVgajsKijB9pjE7upTqgvNtwGyfnz8Sjm6ewwi4JXwvfS",
        "title": "[EP11] [Executable] End the $ENS and EP2 airdrops",
        "body": "This vote proposes [EP11](https://docs.ens.domains/v/governance/governance-proposals/ep11-executable-end-airdrop), reproduced below, be submitted for an onchain vote.\n\n# Abstract\nThe $ENS airdrop can be terminated at any time on or after May 4, 2022 by a call from the DAO, transferring remaining tokens to an address it specifies. The EP2 airdrop can be terminated at any time by revoking the token approval given to it by the DAO. This EP proposes to execute both of these actions on or shortly after May 4, 2022.\n\n# Specification\n - Call 'sweep' on the ENS token contract, specifying the DAO wallet as target address.\n - Call 'approve' on the ENS token contract, specifying the EP2 airdrop contract and an allowance of 0.\n\n# Transactions\n<table>\n    <tr>\n        <th>Address</th>\n        <th>Value</th>\n        <th>Function</th>\n        <th>Argument</th>\n        <th>Value</th>\n    </tr>\n    <tr>\n        <td>0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72</td>\n        <td>0</td>\n        <td>sweep</td>\n        <td>dest</td>\n        <td>0xFe89cc7aBB2C4183683ab71653C4cdc9B02D44b7</td>\n    </tr>\n    <tr>\n        <td rowspan=2>0xC18360217D8F7Ab5e7c516566761Ea12Ce7F9D72</td>\n        <td rowspan=2>0</td>\n        <td rowspan=2>approve</td>\n        <td>spender</td>\n        <td>0x4A1241C2Cf2fD4a39918BCd738f90Bd7094eC2DC</td>\n    </tr>\n    <tr>\n        <td>amount</td>\n        <td>0</td>\n    </tr>\n</table>",
        "start": 1650489821,
        "end": 1650921821,
        "state": "closed",
        "author": "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
        "created": 1650489827,
        "choices": [
          "For",
          "Against",
          "Abstain"
        ],
        "space": {
          "id": "ens.eth",
          "name": "ENS",
          "members": [
            "0x5A384227B65FA093DEC03Ec34e111Db80A040615",
            "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
            "0x983110309620D911731Ac0932219af06091b6744",
            "0x866B3c4994e1416B7C738B9818b31dC246b95eEE",
            "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
            "0x9297A132AF2A1481441AB8dc1Ce6e243d879eaFD",
            "0x75cac0CEb8A39DdB4942A83AD2aAfaF0C2A3e13f"
          ],
          "avatar": "ipfs://QmSL2X1h1uk26ahSALTw2qKyc61VaySRRstueVMm1Aym3e",
          "symbol": "ENS"
        },
        "scores_state": "final",
        "scores_total": 1683490.2949245246,
        "scores": [
          1671001.3808671176,
          12288.70648686089,
          200.20757054624133
        ],
        "votes": 827,
        "quorum": 0,
        "symbol": "ENS"
      },
      {
        "id": "0x104eb11d42813fadc2b408856e8fa2c10e34dbb4a87abaa2f089ece124263f16",
        "ipfs": "Qme6unqKYhKTymXjB8G8ZWyjNtrskqE8k44m16u1LLv85S",
        "title": "[EP10] [Executable] Fund a DAO-Governed Identity Server",
        "body": "Authors: [Gregory Rocco](https://github.com/obstropolos), [Wayne Chang](https://github.com/wyc)\n\n# Description\nThis proposal is for the funding and establishment of a community-run OIDC Identity Provider Server for Sign-In with Ethereum, maintained by Spruce.\n\nTemperature check originally from [this post](https://discuss.ens.domains/t/a-credibly-neutral-sign-in-with-ethereum-identity-provider-server/11001)\n\n# Abstract\nIn our research, we found that many services wanted to integrate the Sign-In with Ethereum workflow but did not have the ability to add new passwordless authentication methods to their installations.\n\nWe also learned that most services already support OpenID Connect, and were open to adding a new Identity Provider that supported the SIWE workflow. By meeting those services where they are today, we can provide a pragmatic stepping stone towards true decentralization, with an upgrade path to direct authentication. \n\nTo ensure adherence to the vision, it's critical that we collaborate with the ENS DAO on hosting and maintenance of this identity server, ensuring the identity server's governance ultimately resides with the community, whom we believe will always put users first. This would be the world’s first DAO-hosted, transparent identity server.\n\n# Rationale\nThe ENS service and community would benefit from increased adoption of Sign-In with Ethereum due to the enablement of organizations to use ENS as a core touchpoint for a user’s basic identity and information (via ENS profiles).\n\nAdditionally, we believe that a community server could be governed by a credibly neutral party that Ethereum users accept as an intermediary. We think a non-profit or DAO are the right structures to help govern such a server, which is why we would like to collaborate with the ENS DAO on hosting and maintenance.\n\n# Specification and Proposal Request\n\n- **Establish a Subgroup in the Ecosystem Working Group: Community Managed Identity Server**\n    - **$250,000** allocated from the DAO to the Ecosystem WG to fund this Subgroup. \n        - **$75,000** from the allocated budget will be in place for community contributions related to the Subgroup, including grants for development, evangelism, and retroactive rewards for SIWE-related efforts.\n        -  **$175,000** from the allocated budget will go towards Spruce's maintenance contract (see below). Paid 25% upon execution, and then an additional 25% every 3 months. \n    - This Subgroup will support the administration and maintenance of a DAO-run Identity Server for Sign-In with Ethereum. This subgroup will also serve as a support system to help onboard organizations, and evangelize Sign-In with Ethereum to allow users to control their identifiers and use ENS profiles as a base identity.\n    - An important part of duties this group will include creating training, onboarding, and maintenance materials for managing the server on a specified cloud account.\n    - Additionally, the group will be responsible for providing updates to the broader community on the health of the server. \n    - Initial lead: Rocco from Spruce, while continuing to add interested parties to the group for good governance. \n    \n- **A 12-month maintenance contract awarded to Spruce for the continuous monitoring, maintaining, and improving of the deployed Identity Server.**\n    - Spruce will help host a [`siwe-oidc`](https://github.com/spruceid/siwe-oidc) implementation in a lightweight fashion, using a well-known infrastructure provider ultimately administered by the Subgroup.\n        - Spruce will also be responsible for the deployment, and continuous monitoring, maintenance, and improvements on the server throughout the duration of the contract. \n    - If the DAO votes to end the contract funding will be returned against the remaining days of the year and we will provide sufficient training for administrators to transfer those duties to a new organization.\n    - The server is expected to be live within 60 days of this proposal being accepted, assuming that access to the necessary systems and people is provided on a timely basis. \n    - The 1-year contract begins when this proposal is accepted, and there will not be additional setup fees even if there are increased coordination costs to get the service running.",
        "start": 1647385200,
        "end": 1647817200,
        "state": "closed",
        "author": "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
        "created": 1647388261,
        "choices": [
          "For",
          "Against",
          "Abstain"
        ],
        "space": {
          "id": "ens.eth",
          "name": "ENS",
          "members": [
            "0x5A384227B65FA093DEC03Ec34e111Db80A040615",
            "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
            "0x983110309620D911731Ac0932219af06091b6744",
            "0x866B3c4994e1416B7C738B9818b31dC246b95eEE",
            "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
            "0x9297A132AF2A1481441AB8dc1Ce6e243d879eaFD",
            "0x75cac0CEb8A39DdB4942A83AD2aAfaF0C2A3e13f"
          ],
          "avatar": "ipfs://QmSL2X1h1uk26ahSALTw2qKyc61VaySRRstueVMm1Aym3e",
          "symbol": "ENS"
        },
        "scores_state": "final",
        "scores_total": 3147195.5454515377,
        "scores": [
          3112001.299883401,
          19481.448570251767,
          15712.796997885012
        ],
        "votes": 445,
        "quorum": 0,
        "symbol": ""
      },
      {
        "id": "0xe040bdae812af4bd5b3b6e3f46ed1ff4701986c338b827ac8f05807c2b9b9d73",
        "ipfs": "QmcdADQWvrS1d9u5yLybvWgqBVz7x1fxkYdf6crjwsXKk5",
        "title": "[EP9] [Executable] Change to Exponential Premium Price Oracle",
        "body": "# Summary\n\nProposes to deploy Exponential Price Oracle Contract to replace the current Linear Price Oracle Contract.\n\n# Abstract\n\nIn the past we deployed the Linear Premium Oracle as a way to create a distribution mechanism that did not involve gas auctions and bots. This was largely successful and those who wanted a recently expired name could participate in the dutch auction and not have to compete on gas or with bots. Recently with the popularity of ENS increasing, the demand and the price people are willing to pay for these premium names has increased. In response to this TNL quickly drafted a [short-term solution](https://discuss.ens.domains/t/ep5-executable-set-the-temporary-premium-start-price-to-100-000/9336) to raise the premium to 100k, which we felt was the upper limit for what a linear price decay curve could handle.\n\nThere are a couple reasons for this:\n\n1. On a linear curve, if the price is too high the price decreases too fast and the UX is bad for a user who wants an exact price (especially at the lower end of the curve)\n2. If you extend the time period out, the premium lasts for too long. E.g. If we made it 1 million USD and we wanted a similar price decay speed as 100k, we would need to run it for 10 months, which seems unreasonable.\n\nWe can see from the data below, even with the new 100k premium, we have already had a 5-7 domains go for maximum, or close to maximum premium. If a domain sells for the actual premium, it means the dutch auction is not doing its job and so we need to deploy a long-term solution for dealing with premium pricing.\n\n```\nRow\tlabel\tevent_timestamp\tpremium\t\n1\tbbc 2022-01-30 17:46:03 UTC 100230.75321837279\n2\tmets 2022-02-04 17:16:22 UTC 100082.49847319399\n3\tfbi 2022-02-05 06:02:31 UTC 99894.00632472485\n4\tfly 2022-02-04 18:49:00 UTC 99747.22640247621\n5\tups 2022-02-05 07:46:24 UTC 98822.14747808539\n6\tdog 2022-02-06 16:19:05 UTC 92950.09208752771\n7\tubs 2022-02-01 15:31:35 UTC 89633.15081063367\n8\tubi 2022-02-19 17:06:17 UTC 72161.56328771653\n9\tpunks 2022-02-16 00:15:44 UTC 59153.166146336\n10\tomg 2022-02-24 16:05:57 UTC 33214.42499419019\n```\n\nThe long-term solution would be to change the actual curve to something that could start at a very high price, would decrease rapidly at the beginning and slow down at the end so you have better UX for users. And therefore this proposal is to deploy an exponential price curve, that does exactly this. This would allow fairer bidding on both high and low priced names.\n\n# Contract Code\n\nhttps://github.com/ensdomains/ens-contracts/blob/master/contracts/ethregistrar/ExponentialPremiumPriceOracle.sol\n\n# Specification\nCall `setPriceOracle` on `controller.ens.eth`, passing in the address of the deployed `ExponentialPremiumPriceOracle` (TBD).\n```",
        "start": 1647385200,
        "end": 1647817200,
        "state": "closed",
        "author": "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
        "created": 1647388127,
        "choices": [
          "For",
          "Against",
          "Abstain"
        ],
        "space": {
          "id": "ens.eth",
          "name": "ENS",
          "members": [
            "0x5A384227B65FA093DEC03Ec34e111Db80A040615",
            "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
            "0x983110309620D911731Ac0932219af06091b6744",
            "0x866B3c4994e1416B7C738B9818b31dC246b95eEE",
            "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
            "0x9297A132AF2A1481441AB8dc1Ce6e243d879eaFD",
            "0x75cac0CEb8A39DdB4942A83AD2aAfaF0C2A3e13f"
          ],
          "avatar": "ipfs://QmSL2X1h1uk26ahSALTw2qKyc61VaySRRstueVMm1Aym3e",
          "symbol": "ENS"
        },
        "scores_state": "final",
        "scores_total": 3251460.5645871274,
        "scores": [
          3232397.2684851913,
          18523.437620466248,
          539.858481470097
        ],
        "votes": 596,
        "quorum": 0,
        "symbol": ""
      },
      {
        "id": "0xdf7e59e58ab0cf5ee0a591bd65369db3ee5091ae3b7ca696a0d31c2eac9959f5",
        "ipfs": "QmbBTatg2r8bA9xZzT5KrTFNZF3yM27NUDeEUbz8smtFST",
        "title": "[EP8] [Executable] Reimburse True Names for expenses and tax obligations incurred on behalf of the DAO",
        "body": "# Summary\nProposes to reimburse True Names Limited for expenses incurred on behalf of ENS and the DAO.\n\n# Abstract\nSince ENS started allowing registrations using the annual-fee model, revenue from this has accrued to the ENS root multisig, which is controlled by seven individuals drawn from the Ethereum community. In order to shield them from individual tax liability, True Names Limited, the development company responsible for ENS development, historically identified itself as the beneficial owner of these funds, which obliged True Names to pay tax on any income to the multisig.\n\nIn past years True Names has covered this tax bill from its own reserves - primarily out of funds that were collected during the Short Name auction - but in 2021 revenue rose to a level that meant that was no longer sustainable. Accordingly, True Names requested funds from the multisig to cover the anticipated tax, and the multisig agreed.\n\nThe calculation used to determine the tax owing used the actual income to October 20th, plus a 1/12th buffer to cover the anticipated income between the launch of the DAO and its potential request for control of the funds from the keyholders. This total came to $2,163,921 USDC.\n\nHowever, this failed to take into account the enormous uptick in interest that the announcement of the DAO produced, and so falls significantly short of True Names' actual tax obligations for FY 2021. This proposal requests that the DAO sends True Names the remainder of the funds required to cover the multisig's income during the period that True Names was the beneficial owner.\n\nFurther, True Names has incurred the following expenses on behalf of the DAO in January 2022:\n\n![Screenshot from 2022-01-28 09-27-45|617x500](upload://1jcGsmCKdHJpl5D0a7CAKr6Bmmd.png)\n\nWe additionally request the DAO reimburse True Names for these expenses in the total of $48,637.\n\n## Revenue\nRevenue to the multisig came exclusively from ENS name registrations and renewals, and can be calculated from onchain data using [this BigQuery query](https://gist.github.com/Arachnid/dfd374886a3e6b0a0eb17b26703d776a), producing the following results:\n\n|Month|ETH|USD|\n| --- | --- | --- |\n|Jan 2021|411.6875|498484.22|\n|Feb 2021|383.5613|643985.05|\n|Mar 2021|453.5619|776834.28|\n|Apr 2021|429.0654|955345.36|\n|May 2021|243.0624|740165.91|\n|Jun 2021|422.2419|993899.95|\n|Jul 2021|384.6863|811202.23|\n|Aug 2021|849.9890|2563121.38|\n|Sep 2021|728.7825|2490699.18|\n|Oct 2021|500.3753|1863125.83|\n|Nov 2021|1699.4660|7643673.03|\n|**Total**|**6506.4793**|**19980536.41**|\n\n## Tax\nSingapore's company tax rate is 17%, meaning that the tax owing on $19,980,536 comes to $3,396,691. After deducting the $2,163,921 USDC already sent by the multisig, this leaves a shortfall of $1,232,770.\n\n# Specification\nWe request that the DAO send $1,281,407 USDC to coldwallet.ens.eth.",
        "start": 1646082000,
        "end": 1646514000,
        "state": "closed",
        "author": "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
        "created": 1646079981,
        "choices": [
          "For",
          "Against",
          "Abstain"
        ],
        "space": {
          "id": "ens.eth",
          "name": "ENS",
          "members": [
            "0x5A384227B65FA093DEC03Ec34e111Db80A040615",
            "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
            "0x983110309620D911731Ac0932219af06091b6744",
            "0x866B3c4994e1416B7C738B9818b31dC246b95eEE",
            "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
            "0x9297A132AF2A1481441AB8dc1Ce6e243d879eaFD",
            "0x75cac0CEb8A39DdB4942A83AD2aAfaF0C2A3e13f"
          ],
          "avatar": "ipfs://QmSL2X1h1uk26ahSALTw2qKyc61VaySRRstueVMm1Aym3e",
          "symbol": "ENS"
        },
        "scores_state": "final",
        "scores_total": 3438033.0821805634,
        "scores": [
          3177575.3724400513,
          715.3601452412548,
          259742.34959527003
        ],
        "votes": 343,
        "quorum": 0,
        "symbol": ""
      },
      {
        "id": "0x8c05add423e7ab5900113b203326286763d402f88300ebbe65c278ed2488b8d1",
        "ipfs": "QmXMi75wWD6PV2MhzidZce1GEVjmRq2ywpK8FDo2Ct2E5r",
        "title": "[EP7.4] [Executable] Q1 & Q2 2022 Public Goods WG Budget",
        "body": "\n# Summary\nThe Ecosystem WG is requesting funding to start the Q1/Q2 2022 term. The initial request is made up of three components:\n\n1. Elected steward compensation: $12,000 in cDAI\n2. Bounties for ENS Public Goods Request for Proposals program: $50,000 in cDAI\n3. Operational Budget $38,000 in cDAI\n\n**Total for Q1 & Q2: $150,000.00 in cDAI**\n\nThe group will be using the price of cDAI in uniswap to calculate the exact amounts requested. We are using cDAI as a accounting unit as a manner to provide a stable value that will still accrue value while not in utilization and resist dollar depreciation. The group can convert them in DAI when sending out payments and grants. The current price of cDAI orbits around 0.021-0.022 per dai and the total budget would be, in today’s value, about 6.85M cDAI.\n\n**Elected steward compensation**\n\nThe group has 5 elected stewards: Alex (avsa.eth), makoto.eth, sumedha.eth, Scott and Richard Moore (Ricmoo.eth). Two of these steward are appointed by True Names and will not be receiving compensation, and one of the other stewards has elected to forego compensation and therefore we will asking only for a total of 12k USD for the total Steward Compensation. Pay for past months will be sent immediately and the remaining will be streamed until june 30th.\n\n**Bounties for ENS Public Goods Request for Proposals program:**\n\nThe bounties will be distributed in prizes of $1,000, $5,000, and $10,000 for projects that execute on basic implementation of goals elected by the stewards. These are set to be given directly to projects and not spent on operations. Any funds remaining at the end of the term will be either given back to the DAO or rolled in the Public Goods stewards budget for the next term.\n\n**Operational Budget**\n\nThese will encompass tasks like reimbursements for expenses executed by stewards, payment for projects like a website, social media, or compensation for work done in partner integrations. All payments must be approved by at least 3 other stewards and will be executed in the most transparent manner the stewards can find.\n",
        "start": 1646082000,
        "end": 1646514000,
        "state": "closed",
        "author": "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
        "created": 1646079967,
        "choices": [
          "For",
          "Against",
          "Abstain"
        ],
        "space": {
          "id": "ens.eth",
          "name": "ENS",
          "members": [
            "0x5A384227B65FA093DEC03Ec34e111Db80A040615",
            "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
            "0x983110309620D911731Ac0932219af06091b6744",
            "0x866B3c4994e1416B7C738B9818b31dC246b95eEE",
            "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
            "0x9297A132AF2A1481441AB8dc1Ce6e243d879eaFD",
            "0x75cac0CEb8A39DdB4942A83AD2aAfaF0C2A3e13f"
          ],
          "avatar": "ipfs://QmSL2X1h1uk26ahSALTw2qKyc61VaySRRstueVMm1Aym3e",
          "symbol": "ENS"
        },
        "scores_state": "final",
        "scores_total": 3527042.0610064804,
        "scores": [
          3307364.0173048717,
          1334.9391263250066,
          218343.1045752851
        ],
        "votes": 301,
        "quorum": 0,
        "symbol": ""
      },
      {
        "id": "0x29040b3196c4d7109fdb7b55b8bfd5e85dd074d3cb22266e0d94cc42cfad1eb2",
        "ipfs": "QmSLuRNYHizMTx5nvDpebGmd3gM2nmij5rQcBymDvGLKg1",
        "title": "[EP7.3] [Executable] Q1 & Q2 2022 Community WG Budget",
        "body": "## Summary\n\n1. **Community WG Operational Budget:** 115,000 USDC/DAI, 1 ETH, and 650 ENS.\n2. **Elected Steward Compensation:** 27,500 in USDC/DAI.\n\n    **Total USD Value:** ~$155,050.\n\n## Community WG Budget: Q1 & Q2 Steward Term\n### 1. Operational Budget \nThis funding is requested to fulfill the needs of the entire Q1/Q2 term.\n\n|Subgroup Name|Description|USDC/DAI|ETH|$ENS|\n| --- | --- | :---: | :---: | :---: |\n|Learn Docs|Content related to user documentation, tutorials, and case studies.|11,000|0|0|\n|Communications|Provide communications services for the DAO to include a bi-weekly digest, weekly twitter spaces, and other outreach services to drive education and engagement.|10,000|0|100|\n|Onboarding |Facilitate and coordinate weekly onboarding calls about ENS and the DAO. Also, focus on refining the DAO onboarding process.|10,000|0|0|\n|Discord Support Moderation|Provides 24-hr support coverage in the ENS Discord.|66,000|0|0|\n|Translation|Administer translation services for the ENS DAO official documents and website details. |6,000|0|0|\n|Communidad Para Hispanohablantes|Increase onboarding for the native Spanish-speaking community.|2,000|0|0|\n|IRL Outreach |Community engagement focused on in-person events.|10,000|0|0|\n|WG Discretionary Funds |Discretionary funding to be allocated to the above subgroups or facilitate the funding of new subgroups as the council of stewards deem necessary. | 0 |1|550|\n|**Total**||**115,000** |**1** |**650**|\n\n**Note:** This includes subgroups and supports moderation of the ENS Discord. The Discord moderation is a necessary DAO expense carried by the community working group.\n\n### 2. Elected Steward Compensation\nProvide compensation for the three elected Community Stewards @limes , @spencecoin  and @coltron.eth  for the entire Q1/Q2 steward term.\n\n|Description|Compensation|Months #|Stewards #|Total USDC|\n| --- | :---: | :---: | :---: | :---: |\n|Base Compensation|$1,000/month|5.5|3|16,500|\n|Supplemental Compensation|$2,000/month|5.5|-|11,000|\n|**Total**||||**27,500**|\n\n**Note:** *Supplemental compensation shall be distributed to stewards and contributors involved in running operations for the WG. The supplemental compensation will be used in situations where contributors or stewards perform duties beyond what is normally expected. The steward council determines how the supplemental compensation will be split between the stewards based on the contributions of each steward.*\n\n\n\n\n### Considerations\nMultiple parties will approve all funding disbursements using a multi-sig. This budget does not guarantee disbursement, specifically if services rendered to the DAO are incomplete or deemed unsatisfactory. If these situations arise, the working group will review them publicly at the weekly Community Steward Call. \n\nAny funding not used will be re-allocated back to the treasury.\n",
        "start": 1646082000,
        "end": 1646514000,
        "state": "closed",
        "author": "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
        "created": 1646079945,
        "choices": [
          "For",
          "Against",
          "Abstain"
        ],
        "space": {
          "id": "ens.eth",
          "name": "ENS",
          "members": [
            "0x5A384227B65FA093DEC03Ec34e111Db80A040615",
            "0xb8c2C29ee19D8307cb7255e1Cd9CbDE883A267d5",
            "0x983110309620D911731Ac0932219af06091b6744",
            "0x866B3c4994e1416B7C738B9818b31dC246b95eEE",
            "0x0904Dac3347eA47d208F3Fd67402D039a3b99859",
            "0x9297A132AF2A1481441AB8dc1Ce6e243d879eaFD",
            "0x75cac0CEb8A39DdB4942A83AD2aAfaF0C2A3e13f"
          ],
          "avatar": "ipfs://QmSL2X1h1uk26ahSALTw2qKyc61VaySRRstueVMm1Aym3e",
          "symbol": "ENS"
        },
        "scores_state": "final",
        "scores_total": 3214911.942896996,
        "scores": [
          3174794.5088113053,
          35407.708252042285,
          4709.725833647952
        ],
        "votes": 287,
        "quorum": 0,
        "symbol": ""
      }
    ]
  }
}
}
```
