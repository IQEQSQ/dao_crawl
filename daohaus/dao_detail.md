
```typescript

////////////            API            ////////////    
const request_dao_detail = "https://data.daohaus.club/dao/" + "Dao的合约地址"
const respond_dao_detail = [
    {
      "contractAddress": "Dao合约地址",
      "network": "Dao所在的网络",
      "name": "Dao组织名字",
      "description": "Dao组织描述",
      "purpose": "Dao组织愿景",
      "version": "Dao组织版本",
      "slug": "Dao组织口号",
      "tags": [
        "Dao标签1",
        "Dao标签2"
      ],
      "links": {
        "website": "Dao组织网站",
        "twitter": "Dao组织推特",
        "discord": "Dao组织Discord",
        "telegram": "Dao组织电报",
        "medium": "Dao组织Medium",
        "other": "Dao组织其他社交情况"
      }
    }
  ]


////////////            Example            ////////////    

const request_dao_detail_1 = "https://data.daohaus.club/dao/0xb152b115c94275b54a3f0b08c1aa1d21f32a659a"
const respond_dao_detail_1 = [
    {
      "contractAddress": "0xb152b115c94275b54a3f0b08c1aa1d21f32a659a",
      "network": "xdai",
      "name": "MetaCartel xDai",
      "description": "If you want to go fast, go alone. If you want to go far, go together.",
      "purpose": "Grants",
      "version": "2.1",
      "slug": "metacartel-v2-hd",
      "tags": [
        "Ethereum",
        "Clubs"
      ],
      "links": {
        "website": "https://metacartel.org",
        "twitter": "Meta_Cartel",
        "discord": "https://discord.gg/vdeUzHwz2R",
        "telegram": "",
        "medium": "",
        "other": ""
      },
      "avatarImg": "QmUYPn3g6gAxRVAYjhFKzByGn4B5yvVTX12VENvz6bgwiH",
      "proposalConfig": {
        "playlists": [
          {
            "name": "Favorites",
            "id": "favorites",
            "forms": [
              "BUY_SHARES",
              "SHARES_FOR_WORK",
              "TOKEN",
              "GUILDKICK"
            ]
          },
          {
            "name": "The Classics",
            "id": "classics",
            "forms": [
              "MEMBER",
              "FUNDING",
              "TOKEN",
              "TRADE",
              "GUILDKICK",
              "SIGNAL"
            ]
          },
          {
            "name": "Vanilla Minion Classics",
            "id": "vanMinionClassics",
            "forms": [
              "MINION",
              "PAYROLL"
            ]
          },
          {
            "name": "Nifty Minion Classics",
            "id": "niftyMinionClassics",
            "forms": [
              "MINION_NIFTY",
              "PAYROLL_NIFTY"
            ]
          },
          {
            "name": "Safe Minion Classics",
            "id": "safeMinionClassics",
            "forms": [
              "MINION_SAFE_SIMPLE",
              "MINION_BUYOUT_TOKEN",
              "SAFE_TX_BUILDER"
            ]
          }
        ],
        "allForms": {
          "name": "All Proposals",
          "id": "all",
          "forms": [
            "BUY_SHARES",
            "SHARES_FOR_WORK",
            "TOKEN",
            "GUILDKICK",
            "MEMBER",
            "FUNDING",
            "TRADE",
            "SIGNAL",
            "MINION",
            "PAYROLL",
            "MINION_NIFTY",
            "PAYROLL_NIFTY",
            "MINION_SAFE_SIMPLE",
            "MINION_BUYOUT_TOKEN",
            "SAFE_TX_BUILDER"
          ]
        },
        "customData": null
      },
      "customThemeConfig": {
        "primary500": "#9670d1",
        "primaryAlpha": "rgba(150,112,209,0.9)",
        "secondary500": "#6c1096",
        "secondaryAlpha": "rgba(108,16,150,0.75)",
        "bg500": "#9670d1",
        "bgAlpha": "#03061B",
        "bgOverlayOpacity": 0.79,
        "modeAlpha500": "#FFFFFF",
        "headingFont": "Rubik",
        "bodyFont": "Merriweather",
        "monoFont": "JetBrains Mono",
        "avatarImg": "/static/media/Daohaus__Castle--Dark.3084fa93.svg",
        "bgImg": "QmVU4kmrQCpfKkKYDbA5iBa5XxzQCvh9VvVTvwAm6SVaye",
        "daoMeta": {
          "proposals": "Proposals",
          "proposal": "Proposal",
          "bank": "Bank",
          "members": "Cartelians",
          "member": "Cartelian",
          "boosts": "Apps",
          "boost": "App",
          "settings": "Settings",
          "ragequit": "Rage Quit",
          "guildKick": "Guild Kick",
          "minion": "Minion",
          "minions": "Minions"
        }
      },
      "daosquarecco": 0,
      "settings": null,
      "customTermsConfig": {
        "proposals": "Proposals",
        "proposal": "Proposal",
        "bank": "Bank",
        "members": "Cartelians",
        "member": "Cartelian",
        "boosts": "Apps",
        "boost": "App",
        "settings": "Settings",
        "ragequit": "Rage Quit",
        "guildKick": "Guild Kick",
        "minion": "Minion",
        "minions": "Minions"
      },
      "allies": [
        {
          "allyType": "uberHausBurner",
          "isParent": true,
          "allyNetwork": "xdai",
          "ally": "0xb152b115c94275b54a3f0b08c1aa1d21f32a659a"
        },
        {
          "allyType": "uberHausBurner",
          "isParent": true,
          "allyNetwork": "xdai",
          "ally": "0xb152b115c94275b54a3f0b08c1aa1d21f32a659a"
        }
      ],
      "logs": [
        {
          "update": {
            "boostKey": "SAFE_DEV_SUITE",
            "metadata": {},
            "proposalConfig": {
              "playlists": [
                {
                  "name": "Favorites",
                  "id": "favorites",
                  "forms": [
                    "BUY_SHARES",
                    "SHARES_FOR_WORK",
                    "TOKEN",
                    "GUILDKICK"
                  ]
                },
                {
                  "name": "The Classics",
                  "id": "classics",
                  "forms": [
                    "MEMBER",
                    "FUNDING",
                    "TOKEN",
                    "TRADE",
                    "GUILDKICK",
                    "SIGNAL"
                  ]
                },
                {
                  "name": "Vanilla Minion Classics",
                  "id": "vanMinionClassics",
                  "forms": [
                    "MINION",
                    "PAYROLL"
                  ]
                },
                {
                  "name": "Nifty Minion Classics",
                  "id": "niftyMinionClassics",
                  "forms": [
                    "MINION_NIFTY",
                    "PAYROLL_NIFTY"
                  ]
                },
                {
                  "name": "Safe Minion Classics",
                  "id": "safeMinionClassics",
                  "forms": [
                    "MINION_SAFE_SIMPLE",
                    "MINION_BUYOUT_TOKEN",
                    "SAFE_TX_BUILDER"
                  ]
                }
              ],
              "allForms": {
                "name": "All Proposals",
                "id": "all",
                "forms": [
                  "BUY_SHARES",
                  "SHARES_FOR_WORK",
                  "TOKEN",
                  "GUILDKICK",
                  "MEMBER",
                  "FUNDING",
                  "TRADE",
                  "SIGNAL",
                  "MINION",
                  "PAYROLL",
                  "MINION_NIFTY",
                  "PAYROLL_NIFTY",
                  "MINION_SAFE_SIMPLE",
                  "MINION_BUYOUT_TOKEN",
                  "SAFE_TX_BUILDER"
                ]
              },
              "customData": null
            }
          },
          "updatedBy": "0x68d36DcBDD7Bbf206e27134F28103abE7cf972df",
          "createdAt": "2021-12-08T05:33:42.000Z"
        },
        {
          "update": {
            "boostKey": "SPAM_FILTER",
            "metadata": {
              "paymentRequested": "10000000000000000000",
              "paymentToken": "0xe91d153e0b41518a2ce8dd3d7944fa863463a97d",
              "membersOnly": false
            }
          },
          "updatedBy": "0xBaf6e57A3940898fd21076b139D4aB231dCbBc5f",
          "createdAt": "2021-11-28T18:59:36.000Z"
        },
        {
          "update": {
            "boostKey": "SPAM_FILTER",
            "metadata": {
              "paymentRequested": "10000000000000000000",
              "paymentToken": "0xe91d153e0b41518a2ce8dd3d7944fa863463a97d",
              "active": "true"
            }
          },
          "updatedBy": "0x68d36DcBDD7Bbf206e27134F28103abE7cf972df",
          "createdAt": "2022-05-17T18:36:18.000Z"
        },
        {
          "update": {
            "boostKey": "SPAM_FILTER",
            "metadata": {
              "paymentRequested": "0",
              "paymentToken": "0xe91d153e0b41518a2ce8dd3d7944fa863463a97d",
              "active": false
            }
          },
          "updatedBy": "0x68d36DcBDD7Bbf206e27134F28103abE7cf972df",
          "createdAt": "2022-05-17T18:35:01.000Z"
        },
        {
          "update": {
            "boostKey": "SPAM_FILTER",
            "metadata": {
              "paymentRequested": "10000000000000000000",
              "paymentToken": "0xe91d153e0b41518a2ce8dd3d7944fa863463a97d",
              "active": false
            }
          },
          "updatedBy": "0x68d36DcBDD7Bbf206e27134F28103abE7cf972df",
          "createdAt": "2022-05-17T18:36:01.000Z"
        },
        {
          "update": {
            "boostKey": "SPAM_FILTER",
            "metadata": {
              "paymentRequested": "10000000000000000000",
              "paymentToken": "0xe91d153e0b41518a2ce8dd3d7944fa863463a97d",
              "active": "true"
            }
          },
          "updatedBy": "0x68d36DcBDD7Bbf206e27134F28103abE7cf972df",
          "createdAt": "2021-11-30T03:12:57.000Z"
        }
      ],
      "boosts": {
        "SNAPSHOT": {
          "active": true,
          "metadata": {
            "space": "metacartel.eth"
          }
        },
        "WRAP_N_ZAP": {
          "active": true,
          "metadata": {}
        },
        "DISCORD": {
          "active": true,
          "metadata": [
            {
              "type": "discord",
              "channelId": "769698426837139466",
              "active": true,
              "actions": [
                "votingPeriod",
                "rageQuit",
                "newProposal"
              ]
            }
          ]
        },
        "SAFE_DEV_SUITE": {
          "active": true,
          "metadata": {}
        },
        "MOLOCH_TOKEN": {
          "active": true,
          "metadata": {}
        },
        "MINTGATE": {
          "active": true,
          "metadata": {}
        },
        "SPAM_FILTER": {
          "active": true,
          "metadata": {
            "paymentRequested": "10000000000000000000",
            "paymentToken": "0xe91d153e0b41518a2ce8dd3d7944fa863463a97d"
          }
        },
        "UberHaus minion": [
          "0x3cea440fb5be559d4c1218b2c3ed74dc973147ad"
        ],
        "vanilla minion": [
          "0x04639d737c4ec157e99796778fe2596276e86851"
        ],
        "nifty minion": [
          "0xb50a189d92306c0df61ef9d020be0ea14250316d"
        ],
        "SAFE MINION V0": [
          "0x6181d7c7d3256068cd11b95c811ec23edbb39731",
          "0x16852e46732def952802f34b598370015a1fa054",
          "0xb8eb2970ab83d0dabce3406dde440daf98349cb3"
        ]
      }
    }
  ]

```
