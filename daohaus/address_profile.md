
```typescript

////////////            API            ////////////    
const request_address_profile = "https://ipfs.3box.io/profile?address=" + "钱包地址"
const respond_address_profile = {
    "website": "个人网址",
    "description": "个人描述",
    "year": "出生年月",
    "major": "专业",
    "degree": "学历",
    "school": "学校",
    "location": "地点",
    "memberSince": "加入Dao时间",
    "name": "名字",
    "proof_did": "完成验证证明",
    "proof_github": "github账户验证证明",
    "proof_twitter": "推特账户验证证明",
    "employer": "雇主"
}


////////////            Example            ////////////    

const request_address_profile_1 = "https://ipfs.3box.io/profile?address=0x86aecfc1e3973108ce14b9b741a99d3466127170"
const respond_address_profile_1 = {
    "website": "https://HaveANiceDay.wtf",
    "proof_github": "https://gist.githubusercontent.com/tbull666/c2194d74ab84f2cb944bef04d901f7c6/raw/ecb9aa2cf3fac3c8bb6be0658da4d543f313ab27/tburdgit",
    "proof_twitter": "eyJ0eXAiOiJKV1QiLCJhbGciOiJFUzI1NksifQ.eyJpYXQiOjE2MzI2NzUzNTgsInN1YiI6ImRpZDozOmJhZnlyZWlnbmx0bjVzdnJoN2hxNG9xNnczano0aWlkM2lkZ3N3dnd0dW5lcWdhMm9yb2FwNXBtb2FhIiwiY2xhaW0iOnsidHdpdHRlcl9oYW5kbGUiOiJ0aW10aW1lIiwidHdpdHRlcl9wcm9vZiI6Imh0dHBzOi8vdHdpdHRlci5jb20vdGltdGltZS9zdGF0dXMvMTQ0MjE3MTAyNTkwMzQ3MjY0NSJ9LCJpc3MiOiJkaWQ6aHR0cHM6dmVyaWZpY2F0aW9ucy4zYm94LmlvIn0.BAMVaO1pNoiibMLSfz2uXYhn0G945RyXPNULtpo3_v8piTo5-mr69HsB4-1EJ-FKHtC3vBbV7Vv7ARdxbsK1TQ",
    "description": "Visual Journalist, humanitarian, river-rat, \n                    sailor and art creator. \nhttps://www.app.rarible.com/tburd\nhttps://www.twitter.com/timtime \n",
    "image": [
        {
            "@type": "ImageObject",
            "contentUrl": {
                "/": "QmQiB8jDsMvmv3bENZirw3qcXLo4q2bBhLd46UNT2LYVx6"
            }
        }
    ],
    "coverPhoto": [
        {
            "@type": "ImageObject",
            "contentUrl": {
                "/": "QmQ4SS9BJReQfYDy7ZoV31sWTBvrdDna918b44knVWHrFN"
            }
        }
    ],
    "emoji": "🕊️",
    "year": "2008",
    "major": "Visual Journalism ",
    "degree": "B.A.",
    "school": "Brooks Institute of Photography ",
    "location": "Quarantine ",
    "memberSince": "Alpha",
    "name": "TBURD",
    "proof_did": "eyJ0eXAiOiJKV1QiLCJhbGciOiJFUzI1NksifQ.eyJpYXQiOjE2MDY2NjkzMjIsImlzcyI6ImRpZDozOmJhZnlyZWlnbmx0bjVzdnJoN2hxNG9xNnczano0aWlkM2lkZ3N3dnd0dW5lcWdhMm9yb2FwNXBtb2FhIn0.XrMeoO4C2PJo58XQZTzilNSBMSegzXAKWwq1gNsAiz2JNQwE9Nw8yrIfaLhQSisMHKqzgYQh_pSfLj51vFQfkw"
}

const request_address_profile2 = "https://ipfs.3box.io/profile?address=0x15c6ac4cf1b5e49c44332fb0a1043ccab19db80a"
const respond_address_profile2 = {
    "emoji": "🌯",
    "proof_did": "eyJ0eXAiOiJKV1QiLCJhbGciOiJFUzI1NksifQ.eyJpYXQiOjE2MDkyNzY5MjIsImlzcyI6ImRpZDozOmJhZnlyZWlheW5jd3lxc2Z3bWFrMm1sY2tua2s3NXI3Mm9jM3psNXprajJ0ejdvZXRpanJvMnd2cmlhIn0.Gg5xjviOy8FXGRWSLVGy8j1-X3pkJ9C6KhwsizFL0FC57ZQOMDtH6jagxrA6_kqA7Kcq-ZXT0JIx67fXDNWyVA",
    "image": [
        {
            "@type": "ImageObject",
            "contentUrl": {
                "/": "QmUcs5QPu5h4xSDQJixrXr8w2h4HcgFQtv1gSKpJgBz2yE"
            }
        }
    ],
    "employer": "Raid Guild",
    "name": "Spencer Graham",
    "memberSince": "Sat Jun 13 2020 14:24:08 GMT-0500 (Central Daylight Time)"
}


const request_address_profile3 = "https://ipfs.3box.io/profile?address=0x1c9e5aba9bce815ed3bb7d9455931b84c56d5114"
const respond_address_profile3 = {
    "proof_did": "eyJ0eXAiOiJKV1QiLCJhbGciOiJFUzI1NksifQ.eyJpYXQiOjE1OTk4ODgyMTUsImlzcyI6ImRpZDozOmJhZnlyZWlnb2ViNno1dTd0NHFrdWVvZWZ0NTRoYWwyY3VpcTNhem40dWg0eTN4NmU1Ymlya3Z3bzNxIn0.2AnZfvHMSADK6jWfPbxEq_rGNpm4wNr01M6C7lDynlnQj23XMw4KATtlvBYXzPrkfP7jKCkh9XiJWpz-B6O15Q",
    "proof_twitter": "eyJ0eXAiOiJKV1QiLCJhbGciOiJFUzI1NksifQ.eyJpYXQiOjE1Njg2NzY3MDMsInN1YiI6ImRpZDptdXBvcnQ6UW1OemNreXJRazVhc3V4dUJmNXhxNERNSmk1ZXB5UWo2NGFVMnlBNzhBbnE4YSIsImNsYWltIjp7InR3aXR0ZXJfaGFuZGxlIjoiamVtZW5nZXIiLCJ0d2l0dGVyX3Byb29mIjoiaHR0cHM6Ly90d2l0dGVyLmNvbS9qZW1lbmdlci9zdGF0dXMvMTE3Mzc0MTI1MjUyMjYwMjQ5NiJ9LCJpc3MiOiJkaWQ6aHR0cHM6dmVyaWZpY2F0aW9ucy4zYm94LmlvIn0.oT8xh_uD9fAQDBBee9c15EpuX4WvEPj0Kuw7Q0uAGeoF4Q4to0R9Fim6bbcnl5hy6BnFLhMYcE5VB6g5yjtyaA",
    "proof_github": "https://gist.githubusercontent.com/jemenger/7722ae34bd1caf863e01dcb7d87f02b1/raw/71d6015bbee2cc56664c7169f5f4b65cdd935df5/3Box%20Verification",
    "emoji": "✨",
    "website": "https://twitter.com/jemenger",
    "location": "Planet Ethereum",
    "name": "Je-Meng",
    "memberSince": "Mon Sep 16 2019 16:20:45 GMT-0700 (Pacific Daylight Time)"
  }

```
