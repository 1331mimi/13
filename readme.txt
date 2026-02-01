{
  "dns": {
    "hosts": {
      "domain:googleapis.cn": "googleapis.com",
      "dns.alidns.com": [
        "223.5.5.5",
        "223.6.6.6",
        "2400:3200::1",
        "2400:3200:baba::1"
      ],
      "one.one.one.one": [
        "1.1.1.1",
        "1.0.0.1",
        "2606:4700:4700::1111",
        "2606:4700:4700::1001"
      ],
      "dns.cloudflare.com": [
        "104.16.132.229",
        "104.16.133.229",
        "2606:4700::6810:84e5",
        "2606:4700::6810:85e5"
      ],
      "cloudflare-dns.com": [
        "104.16.248.249",
        "104.16.249.249",
        "2606:4700::6810:f8f9",
        "2606:4700::6810:f9f9"
      ],
      "dot.pub": [
        "1.12.12.12",
        "120.53.53.53"
      ],
      "dns.google": [
        "8.8.8.8",
        "8.8.4.4",
        "2001:4860:4860::8888",
        "2001:4860:4860::8844"
      ],
      "dns.quad9.net": [
        "9.9.9.9",
        "149.112.112.112",
        "2620:fe::fe",
        "2620:fe::9"
      ],
      "common.dot.dns.yandex.net": [
        "77.88.8.8",
        "77.88.8.1",
        "2a02:6b8::feed:0ff",
        "2a02:6b8:0:1::feed:0ff"
      ],
      "ipbaz.ping-box.com": "188.114.98.0",
      "fi1.persianhostnet.ir": "46.38.149.121",
      "chat.openai.com": [
        "172.64.150.28",
        "104.18.37.228"
      ],
      "pqh38v3.viripdirect.shop": "45.82.251.43"
    },
    "servers": [
      "1.1.1.1"
    ],
    "tag": "dns-module"
  },
  "inbounds": [
    {
      "listen": "127.0.0.1",
      "port": 10808,
      "protocol": "socks",
      "settings": {
        "auth": "noauth",
        "udp": true,
        "userLevel": 8
      },
      "sniffing": {
        "destOverride": [
          "http",
          "tls"
        ],
        "enabled": true,
        "routeOnly": false
      },
      "tag": "socks"
    }
  ],
  "log": {
    "loglevel": "warning"
  },
  "observatory": {
    "enableConcurrency": true,
    "probeInterval": "3m",
    "probeUrl": "https://www.gstatic.com/generate_204",
    "subjectSelector": [
      "proxy-"
    ]
  },
  "outbounds": [
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "ipbaz.ping-box.com",
            "port": 8443,
            "users": [
              {
                "encryption": "none",
                "id": "829658bf-03c4-4c28-81e9-dd6ea141b2d0",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "sockopt": {
          "domainStrategy": "UseIP",
          "happyEyeballs": {
            "interleave": 2,
            "maxConcurrentTry": 4,
            "prioritizeIPv6": false,
            "tryDelayMs": 250
          }
        },
        "tlsSettings": {
          "allowInsecure": false,
          "alpn": [
            "http/1.1"
          ],
          "fingerprint": "chrome",
          "serverName": "5jq7fvwpqt5owo2fi198sa6qoxznkzfea7en4m3xroeqrt3u3q.zjde5.de5.net",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "5jq7fvwpqt5owo2fi198sa6qoxznkzfea7en4m3xroeqrt3u3q.zjde5.de5.net"
          },
          "path": "/vpnowl-vpnowl-vpnowl-vpnowl-vpnowl-vpnowl-vpnowl-vpnowl-vpnowl-vpnowl-vpnowl-vpnowl-vpnowl-vpnowl-vpnowl-vpnowl?ed=2560"
        }
      },
      "tag": "proxy-1"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "185.214.74.184",
            "port": 443,
            "users": [
              {
                "encryption": "none",
                "flow": "xtls-rprx-vision",
                "id": "2275661d-a9b7-522d-99e6-a4d42cb04fa0",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "tcp",
        "realitySettings": {
          "allowInsecure": false,
          "fingerprint": "chrome",
          "publicKey": "PEMF0zJRT97z18eQUFk5jT5sBk1bYZ-Q2PxeFkfEKTQ",
          "serverName": "apple.com",
          "shortId": "ffffffffff",
          "show": false
        },
        "security": "reality",
        "tcpSettings": {
          "header": {
            "type": "none"
          }
        }
      },
      "tag": "proxy-2"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "172.66.132.196",
            "port": 443,
            "users": [
              {
                "encryption": "none",
                "id": "d0298536-d670-4045-bbb1-ddd5ea68683e",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "serverName": "a.azadnet003.ddns-ip.net",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "a.azadnet003.ddns-ip.net"
          },
          "path": "/"
        }
      },
      "tag": "proxy-3"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "fi1.persianhostnet.ir",
            "port": 5121,
            "users": [
              {
                "encryption": "none",
                "id": "38cc3dff-5114-429f-9a45-fed484086c47",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "tcp",
        "sockopt": {
          "domainStrategy": "UseIP",
          "happyEyeballs": {
            "interleave": 2,
            "maxConcurrentTry": 4,
            "prioritizeIPv6": false,
            "tryDelayMs": 250
          }
        },
        "tcpSettings": {
          "header": {
            "type": "none"
          }
        }
      },
      "tag": "proxy-4"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "104.21.227.134",
            "port": 2096,
            "users": [
              {
                "encryption": "none",
                "id": "686c62d9-17a7-43c9-a40a-f6747df60a9f",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "fingerprint": "chrome",
          "serverName": "ca.adobe-connect.top",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "ca.adobe-connect.top"
          },
          "path": "/"
        }
      },
      "tag": "proxy-5"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "104.17.163.123",
            "port": 8443,
            "users": [
              {
                "encryption": "none",
                "id": "83adcc98-ac23-4e51-9ae0-788a73fd9939",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "alpn": [
            "http/1.1"
          ],
          "fingerprint": "chrome",
          "serverName": "vjv62pggz1658fuliaf9lri7rra85l8utox0kjtogve4whop.zjde5.de5.net",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "vjv62pggz1658fuliaf9lri7rra85l8utox0kjtogve4whop.zjde5.de5.net"
          },
          "path": "/?ed=2560"
        }
      },
      "tag": "proxy-6"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "104.17.164.123",
            "port": 8443,
            "users": [
              {
                "encryption": "none",
                "id": "07a21b46-f4a6-47b6-89d1-98375c44262f",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "serverName": "1o1qulwpyj16e5ywam0gb7za0957ey3ujj8odofs87th5erf5bqkf9.zjde5.de5.net",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "1o1qulwpyj16e5ywam0gb7za0957ey3ujj8odofs87th5erf5bqkf9.zjde5.de5.net"
          },
          "path": "/?ed"
        }
      },
      "tag": "proxy-7"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "212.111.85.1",
            "port": 8443,
            "users": [
              {
                "encryption": "none",
                "flow": "xtls-rprx-vision",
                "id": "80115515-eb00-4d28-8f02-66b3e3e6a515",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "tcp",
        "realitySettings": {
          "allowInsecure": false,
          "fingerprint": "chrome",
          "publicKey": "Qddpg8luihgzgx4g4uMJklXzlrMCd8L1igJSWrRUvSc",
          "serverName": "m.vk.ru",
          "shortId": "1929ef620e9b34f5",
          "show": false
        },
        "security": "reality",
        "tcpSettings": {
          "header": {
            "type": "none"
          }
        }
      },
      "tag": "proxy-8"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "188.114.98.0",
            "port": 443,
            "users": [
              {
                "encryption": "none",
                "id": "3f0f36f5-f091-45c5-88c9-4bcc545b922c",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "fingerprint": "chrome",
          "serverName": "hetz.x-smm.com",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "hetz.x-smm.com"
          },
          "path": "/45.76.183.217=49292"
        }
      },
      "tag": "proxy-9"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "104.18.15.19",
            "port": 8443,
            "users": [
              {
                "encryption": "none",
                "id": "0665cf1e-0df8-4981-a8de-a366e37c0866",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "alpn": [
            "http/1.1"
          ],
          "fingerprint": "chrome",
          "serverName": "xdol7mayq6wu5kil7wjyrni7o8tnydsafcmhfhn7g6rimbw5o2g6mlm.zjde5.de5.net",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "xdol7mayq6wu5kil7wjyrni7o8tnydsafcmhfhn7g6rimbw5o2g6mlm.zjde5.de5.net"
          },
          "path": "/?ed=2560"
        }
      },
      "tag": "proxy-10"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "chat.openai.com",
            "port": 443,
            "users": [
              {
                "encryption": "none",
                "id": "396c904b-4b62-4334-b793-ee25fc0c61cc",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "sockopt": {
          "domainStrategy": "UseIP",
          "happyEyeballs": {
            "interleave": 2,
            "maxConcurrentTry": 4,
            "prioritizeIPv6": false,
            "tryDelayMs": 250
          }
        },
        "tlsSettings": {
          "allowInsecure": false,
          "serverName": "pages.dev",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "8vmU06cxdz59m931xnREgj8qpnoq1-06.pages.dev"
          },
          "path": "/eyJqdW5rIjoiTHczMWlhREZIb0ljUDhoaCIsInByb3RvY29sIjoidmwiLCJtb2RlIjoicHJveHlpcCIsInBhbmVsSVBzIjpbXX0=?ed=2560"
        }
      },
      "tag": "proxy-11"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "212.111.84.187",
            "port": 8443,
            "users": [
              {
                "encryption": "none",
                "flow": "xtls-rprx-vision",
                "id": "d4d031ec-0ba6-486a-aa0c-dce2b7cb8933",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "tcp",
        "realitySettings": {
          "allowInsecure": false,
          "fingerprint": "chrome",
          "publicKey": "Qddpg8luihgzgx4g4uMJklXzlrMCd8L1igJSWrRUvSc",
          "serverName": "m.vk.ru",
          "shortId": "887c0d72e771a934",
          "show": false
        },
        "security": "reality",
        "tcpSettings": {
          "header": {
            "type": "none"
          }
        }
      },
      "tag": "proxy-12"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "pqh38v3.viripdirect.shop",
            "port": 8880,
            "users": [
              {
                "encryption": "none",
                "id": "8dc7722c-2767-4eea-a28b-2f8daacc07e3",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "grpcSettings": {
          "authority": "",
          "health_check_timeout": 20,
          "idle_timeout": 60,
          "multiMode": false,
          "serviceName": ""
        },
        "network": "grpc",
        "sockopt": {
          "domainStrategy": "UseIP",
          "happyEyeballs": {
            "interleave": 2,
            "maxConcurrentTry": 4,
            "prioritizeIPv6": false,
            "tryDelayMs": 250
          }
        }
      },
      "tag": "proxy-13"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "trojan",
      "settings": {
        "servers": [
          {
            "address": "94.140.0.1",
            "level": 8,
            "ota": false,
            "password": "bpb-trojan",
            "port": 443
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "alpn": [
            "h2"
          ],
          "fingerprint": "chrome",
          "serverName": "singbox.lu567890.us.kg",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "singbox.lu567890.us.kg"
          },
          "path": "/tr?ed=2560"
        }
      },
      "tag": "proxy-14"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "94.184.24.7",
            "port": 1027,
            "users": [
              {
                "encryption": "none",
                "id": "ba4c2726-fd93-411c-a999-99b5868cb8ba",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "tcp",
        "tcpSettings": {
          "header": {
            "request": {
              "headers": {
                "Connection": [
                  "keep-alive"
                ],
                "Host": [
                  "gharar.ir",
                  "igap.net",
                  "skyroom.online"
                ],
                "Pragma": "no-cache",
                "Accept-Encoding": [
                  "gzip, deflate"
                ],
                "User-Agent": [
                  "Mozilla/5.0 (Linux; Android 10; K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/126.0.6478.122 Mobile Safari/537.36"
                ]
              },
              "method": "GET",
              "path": [
                "/"
              ],
              "version": "1.1"
            },
            "type": "http"
          }
        }
      },
      "tag": "proxy-15"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "ipbaz.ping-box.com",
            "port": 2053,
            "users": [
              {
                "encryption": "none",
                "id": "b30299bb-fd03-4a9c-a28b-62f6922ffbff",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "sockopt": {
          "domainStrategy": "UseIP",
          "happyEyeballs": {
            "interleave": 2,
            "maxConcurrentTry": 4,
            "prioritizeIPv6": false,
            "tryDelayMs": 250
          }
        },
        "tlsSettings": {
          "allowInsecure": false,
          "alpn": [
            "h3",
            "h2",
            "http/1.1"
          ],
          "fingerprint": "chrome",
          "serverName": "hz.badomzamini.uk",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "hz.badomzamini.uk"
          },
          "path": "/latest?ed=2560"
        }
      },
      "tag": "proxy-16"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "104.18.26.90",
            "port": 2095,
            "users": [
              {
                "encryption": "none",
                "id": "b30299bb-fd03-4a9c-a28b-62f6922ffbff",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "httpupgradeSettings": {
          "host": "ba2.badomzamini.uk",
          "path": "/?ed=2095"
        },
        "network": "httpupgrade"
      },
      "tag": "proxy-17"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "104.17.162.123",
            "port": 8443,
            "users": [
              {
                "encryption": "none",
                "id": "8f1a15bf-a352-4c32-aee2-957039a6847b",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "alpn": [
            "http/1.1"
          ],
          "fingerprint": "chrome",
          "serverName": "6nwf5rauksz8126xm.zjde5.de5.net",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "6nwf5rauksz8126xm.zjde5.de5.net"
          },
          "path": "/?ed=2560"
        }
      },
      "tag": "proxy-18"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "104.17.162.123",
            "port": 8443,
            "users": [
              {
                "encryption": "none",
                "id": "83f03646-fb28-44cc-9d2c-8853f6c09285",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "alpn": [
            "http/1.1"
          ],
          "fingerprint": "random",
          "serverName": "r4fnviw9jl4i4rx.zjde5.de5.net",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "r4fnviw9jl4i4rx.zjde5.de5.net"
          },
          "path": "/?ed=2560"
        }
      },
      "tag": "proxy-19"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "trojan",
      "settings": {
        "servers": [
          {
            "address": "94.140.0.1",
            "level": 8,
            "ota": false,
            "password": "bpb-trojan",
            "port": 443
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "fingerprint": "chrome",
          "serverName": "singbox.lu567890.us.kg",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "singbox.lu567890.us.kg"
          },
          "path": "/tr?ed=2560"
        }
      },
      "tag": "proxy-20"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "ip.notomarosww.com",
            "port": 8443,
            "users": [
              {
                "encryption": "none",
                "id": "829658bf-03c4-4c28-81e9-dd6ea141b2d0",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "alpn": [
            "http/1.1"
          ],
          "fingerprint": "chrome",
          "serverName": "5jq7fvwpqt5owo2fi198sa6qoxznkzfea7en4m3xroeqrt3u3q.zjde5.de5.net",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "5jq7fvwpqt5owo2fi198sa6qoxznkzfea7en4m3xroeqrt3u3q.zjde5.de5.net"
          },
          "path": "mehrosaboran?ed=2560"
        }
      },
      "tag": "proxy-21"
    },
    {
      "mux": {
        "concurrency": -1,
        "enabled": false
      },
      "protocol": "vless",
      "settings": {
        "vnext": [
          {
            "address": "66.81.247.155",
            "port": 443,
            "users": [
              {
                "encryption": "none",
                "id": "d0298536-d670-4045-bbb1-ddd5ea68683e",
                "level": 8
              }
            ]
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "alpn": [
            "http/1.1"
          ],
          "serverName": "a.azadnet003.ddns-ip.net",
          "show": false
        },
        "wsSettings": {
          "headers": {
            "Host": "a.azadnet003.ddns-ip.net"
          },
          "path": "/Telegram@V2rayAlpha/?ed=2560"
        }
      },
      "tag": "proxy-22"
    },
    {
      "protocol": "freedom",
      "settings": {
        "domainStrategy": "UseIP"
      },
      "tag": "direct"
    },
    {
      "protocol": "blackhole",
      "settings": {
        "response": {
          "type": "http"
        }
      },
      "tag": "block"
    }
  ],
  "policy": {
    "levels": {
      "8": {
        "connIdle": 300,
        "downlinkOnly": 1,
        "handshake": 4,
        "uplinkOnly": 1
      }
    },
    "system": {
      "statsOutboundUplink": true,
      "statsOutboundDownlink": true
    }
  },
  "remarks": "other'sIntelligent Selection",
  "routing": {
    "balancers": [
      {
        "selector": [
          "proxy-"
        ],
        "strategy": {
          "type": "leastPing"
        },
        "tag": "proxy-round"
      }
    ],
    "domainStrategy": "AsIs",
    "rules": [
      {
        "inboundTag": [
          "domestic-dns"
        ],
        "outboundTag": "direct",
        "type": "field"
      },
      {
        "balancerTag": "proxy-round",
        "inboundTag": [
          "dns-module"
        ],
        "type": "field"
      },
      {
        "balancerTag": "proxy-round",
        "network": "tcp,udp",
        "type": "field"
      }
    ]
  },
  "stats": {}
}