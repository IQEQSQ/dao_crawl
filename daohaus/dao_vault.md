```typescript
////////////            API            ////////////
const request_dao_vault = fetch("https://data.daohaus.club/dao/vaults", {
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
    body: '{"network":"xdai","minions":["Dao地址1","Dao地址2","Dao地址3","Dao地址4"]}',
    method: "POST",
    mode: "cors",
    credentials: "omit",
});

const respond_dao_vault = [
    {
        address: "合约地址",
        safeAddress: null,
        type: "类型",
        minionType: "minion类型",
        name: "Dao名字",
        molochAddress: "moloch地址",
        erc20s: ["发行的ERC20代币列表"],
        networkTokenBalance: {},
        crossChainMinion: false,
        foreignChainId: null,
        foreignSafeAddress: null,
        nfts: ["发行的NFT列表"],
        balanceHistory: [
            {
                value: "26471654941502615323899",
                tokenDecimals: "18",
                tokenAddress: "0xe91d153e0b41518a2ce8dd3d7944fa863463a97d",
                tokenName: "Wrapped XDAI",
                tokenSymbol: "WXDAI",
                timestamp: "1649087560",
                deposit: false,
                transactionHash:
                    "0x4bafd788ed64084d73c2f6ffe6f367b8a049c92cb4f2dad72de4f000628d2349",
                gasUsed: "91476",
                from: "0x04639d737c4ec157e99796778fe2596276e86851",
                to: "0xb152b115c94275b54a3f0b08c1aa1d21f32a659a",
                balance: -2.6471654941502615e22,
            }
        ],
        currentBalance: 0,
    },
];

////////////            Example            ////////////

const request_dao_vault_1 = fetch("https://data.daohaus.club/dao/vaults", {
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

const respond_dao_vault_1 = [
   {
  "address": "0x16852e46732def952802f34b598370015a1fa054",
  "safeAddress": "0x00f2e0c3fb3e816357867127f1ff848a99bdd3a5",
  "type": "minion",
  "minionType": "SAFE MINION V0",
  "name": "Spicier Bank 🌶",
  "molochAddress": "0xb152b115c94275b54a3f0b08c1aa1d21f32a659a",
  "erc20s": [
    {
      "balance": "44500000000000000000",
      "contractAddress": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "decimals": "18",
      "name": "Wrapped Ether on xDai",
      "symbol": "WETH",
      "type": "ERC-20",
      "id": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "tokenAddress": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "tokenBalance": "44500000000000000000",
      "tokenName": "Wrapped Ether on xDai",
      "mainnetAddress": "0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2",
      "usd": 2026.09,
      "logoURI": "https://assets.coingecko.com/coins/images/2518/small/weth.png?1628852295",
      "logoUri": "https://assets.coingecko.com/coins/images/2518/small/weth.png?1628852295"
    },
    {
      "balance": "3950000000000000000000",
      "contractAddress": "0xe91d153e0b41518a2ce8dd3d7944fa863463a97d",
      "decimals": "18",
      "name": "Wrapped XDAI",
      "symbol": "WXDAI",
      "type": "ERC-20",
      "id": "0xe91d153e0b41518a2ce8dd3d7944fa863463a97d",
      "tokenAddress": "0xe91d153e0b41518a2ce8dd3d7944fa863463a97d",
      "tokenBalance": "3950000000000000000000",
      "tokenName": "Wrapped XDAI",
      "mainnetAddress": "0x6b175474e89094c44da98b954eedeac495271d0f",
      "usd": 1.003,
      "logoURI": "https://assets.coingecko.com/coins/images/9956/small/4943.png?1636636734",
      "logoUri": "https://assets.coingecko.com/coins/images/9956/small/4943.png?1636636734"
    }
  ],
  "networkTokenBalance": {},
  "crossChainMinion": false,
  "foreignChainId": null,
  "foreignSafeAddress": null,
  "nfts": [],
  "balanceHistory": [
    {
      "value": "84000000000000000000",
      "tokenDecimals": "18",
      "tokenAddress": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "tokenName": "Wrapped Ether on xDai",
      "tokenSymbol": "WETH",
      "timestamp": "1646760145",
      "deposit": true,
      "transactionHash": "0x7f80a248f2496da4ddfd5ea4943fe7d881b20f003fd4135f6ab55d95f2fc58bb",
      "gasUsed": "146035",
      "from": "0xcff1d7623b840e675de4635dd556d51cb1831bb4",
      "to": "0x00f2e0c3fb3e816357867127f1ff848a99bdd3a5",
      "balance": 84000000000000000000
    },
    {
      "value": "3750000000000000000",
      "tokenDecimals": "18",
      "tokenAddress": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "tokenName": "Wrapped Ether on xDai",
      "tokenSymbol": "WETH",
      "timestamp": "1646860055",
      "deposit": false,
      "transactionHash": "0x5c6a50d6b00146a258da56eb61b2ef901bb36abf1d053966acf75e80d882035a",
      "gasUsed": "281260",
      "from": "0x00f2e0c3fb3e816357867127f1ff848a99bdd3a5",
      "to": "0x8c0c36c85192204c8d782f763ff5a30f5ba0192f",
      "balance": 80250000000000000000
    },
    {
      "value": "10000000000000000000",
      "tokenDecimals": "18",
      "tokenAddress": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "tokenName": "Wrapped Ether on xDai",
      "tokenSymbol": "WETH",
      "timestamp": "1646862555",
      "deposit": false,
      "transactionHash": "0x3aac69fe33170c7527b4855a10db835f8a6e77f91c27930dc2d30f31e6c8a09c",
      "gasUsed": "277724",
      "from": "0x00f2e0c3fb3e816357867127f1ff848a99bdd3a5",
      "to": "0x8c0c36c85192204c8d782f763ff5a30f5ba0192f",
      "balance": 70250000000000000000
    },
    {
      "value": "3750000000000000000",
      "tokenDecimals": "18",
      "tokenAddress": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "tokenName": "Wrapped Ether on xDai",
      "tokenSymbol": "WETH",
      "timestamp": "1646935085",
      "deposit": false,
      "transactionHash": "0x1c2db3a52299bbacf73a89932708bc0feee4d2538815a5678573d483bbd60ad6",
      "gasUsed": "260624",
      "from": "0x00f2e0c3fb3e816357867127f1ff848a99bdd3a5",
      "to": "0x8c0c36c85192204c8d782f763ff5a30f5ba0192f",
      "balance": 66500000000000000000
    },
    {
      "value": "10000000000000000000",
      "tokenDecimals": "18",
      "tokenAddress": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "tokenName": "Wrapped Ether on xDai",
      "tokenSymbol": "WETH",
      "timestamp": "1646935140",
      "deposit": false,
      "transactionHash": "0x311b73a1593431e7225c92324e0863a3810feb8632574d23737170ba97fcaab3",
      "gasUsed": "262857",
      "from": "0x00f2e0c3fb3e816357867127f1ff848a99bdd3a5",
      "to": "0x8c0c36c85192204c8d782f763ff5a30f5ba0192f",
      "balance": 56500000000000000000
    },
    {
      "value": "3000000000000000000",
      "tokenDecimals": "18",
      "tokenAddress": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "tokenName": "Wrapped Ether on xDai",
      "tokenSymbol": "WETH",
      "timestamp": "1651266585",
      "deposit": false,
      "transactionHash": "0xc89f5d86987a4f00970f3073a8614aa4ca3a5f911b456f99210df60c6137635b",
      "gasUsed": "224082",
      "from": "0x00f2e0c3fb3e816357867127f1ff848a99bdd3a5",
      "to": "0xb6d052d6f5921d52c1c14b69a02de04f840cefcd",
      "balance": 53500000000000000000
    },
    {
      "value": "3000000000000000000",
      "tokenDecimals": "18",
      "tokenAddress": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "tokenName": "Wrapped Ether on xDai",
      "tokenSymbol": "WETH",
      "timestamp": "1651266585",
      "deposit": false,
      "transactionHash": "0xc89f5d86987a4f00970f3073a8614aa4ca3a5f911b456f99210df60c6137635b",
      "gasUsed": "224082",
      "from": "0x00f2e0c3fb3e816357867127f1ff848a99bdd3a5",
      "to": "0x68d36dcbdd7bbf206e27134f28103abe7cf972df",
      "balance": 50500000000000000000
    },
    {
      "value": "4000000000000000000",
      "tokenDecimals": "18",
      "tokenAddress": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "tokenName": "Wrapped Ether on xDai",
      "tokenSymbol": "WETH",
      "timestamp": "1651266585",
      "deposit": false,
      "transactionHash": "0xc89f5d86987a4f00970f3073a8614aa4ca3a5f911b456f99210df60c6137635b",
      "gasUsed": "224082",
      "from": "0x00f2e0c3fb3e816357867127f1ff848a99bdd3a5",
      "to": "0x914aa366fc6af1cef6d8b98dd24b2842e0d14c39",
      "balance": 46500000000000000000
    },
    {
      "value": "2000000000000000000",
      "tokenDecimals": "18",
      "tokenAddress": "0x6a023ccd1ff6f2045c3309768ead9e68f978f6e1",
      "tokenName": "Wrapped Ether on xDai",
      "tokenSymbol": "WETH",
      "timestamp": "1651266585",
      "deposit": false,
      "transactionHash": "0xc89f5d86987a4f00970f3073a8614aa4ca3a5f911b456f99210df60c6137635b",
      "gasUsed": "224082",
      "from": "0x00f2e0c3fb3e816357867127f1ff848a99bdd3a5",
      "to": "0x5efb9289a919e4116a1e161411c4a0d86c589728",
      "balance": 44500000000000000000
    },
    {
      "value": "3950000000000000000000",
      "tokenDecimals": "18",
      "tokenAddress": "0xe91d153e0b41518a2ce8dd3d7944fa863463a97d",
      "tokenName": "Wrapped XDAI",
      "tokenSymbol": "WXDAI",
      "timestamp": "1652389495",
      "deposit": true,
      "transactionHash": "0xb1eec7ad2eeabced6c2effd3822e3ef76a0826005b506878dde091e1d50de40f",
      "gasUsed": "85712",
      "from": "0x8de017bb26aca9a83b437b8cb46ac7b70d70fe08",
      "to": "0x00f2e0c3fb3e816357867127f1ff848a99bdd3a5",
      "balance": 3.95e+21
    }
  ],
  "currentBalance": 94122.855
}
];
```
