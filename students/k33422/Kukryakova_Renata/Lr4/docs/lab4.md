# Отчет по лабораторной работе 4
## _Реализация клиентской части средствами Vue.js._


## Файлы

* `db.json`

```python
{
  "users": [
    {
      "firstName": "Rina",
      "lastName": "Kuk",
      "email": "rina@gmail.com",
      "password": "123456",
      "coins": [],
      "id": 11
    },
    {
      "firstName": "Rina",
      "lastName": "Kuk",
      "email": "rina@gmail.com",
      "password": "123456",
      "coins": [],
      "id": 12
    },
    {
      "firstName": "Lina",
      "lastName": "Bal",
      "email": "lili@gfhf.com",
      "password": "4352737537",
      "coins": [
        {
          "id": "bitcoin",
          "amount": 10
        }
      ],
      "id": 13
    },
    {
      "firstName": "Tu",
      "lastName": "Tutu",
      "email": "tu@gmail.com",
      "password": "123456789",
      "coins": [],
      "id": 14
    },
    {
      "firstName": "Ru",
      "lastName": "Ruru",
      "email": "ru@gmail.com",
      "password": "13579",
      "coins": [
        {
          "id": "bitcoin",
          "amount": 10
        }
      ],
      "id": 15
    },
    {
      "firstName": "Vi",
      "lastName": "Ka",
      "email": "vi@mail.ru",
      "password": "444rrr",
      "coins": [
        {
          "id": "bitcoin",
          "amount": 13
        }
      ],
      "id": 16
    }
  ],
  "coins": [
    {
      "id": "bitcoin",
      "symbol": "btc",
      "name": "Bitcoin",
      "image": "https://assets.coingecko.com/coins/images/1/large/bitcoin.png?1547033579",
      "current_price": 1272032,
      "market_cap": 24409071471427,
      "market_cap_rank": 1,
      "fully_diluted_valuation": 26711143380579,
      "total_volume": 3137305680118,
      "high_24h": 1284001,
      "low_24h": 1237995,
      "price_change_24h": 34037,
      "price_change_percentage_24h": 2.74941,
      "market_cap_change_24h": 654008711490,
      "market_cap_change_percentage_24h": 2.75313,
      "circulating_supply": 19190137,
      "total_supply": 21000000,
      "max_supply": 21000000,
      "ath": 6075508,
      "ath_change_percentage": -79.06415,
      "ath_date": "2022-03-07T16:43:46.826Z",
      "atl": 2206.43,
      "atl_change_percentage": 57547.75776,
      "atl_date": "2013-07-05T00:00:00.000Z",
      "roi": null,
      "last_updated": "2022-10-26T20:40:15.189Z"
    },
    {
      "id": "ethereum",
      "symbol": "eth",
      "name": "Ethereum",
      "image": "https://assets.coingecko.com/coins/images/279/large/ethereum.png?1595348880",
      "current_price": 95130,
      "market_cap": 11465787949177,
      "market_cap_rank": 2,
      "fully_diluted_valuation": 11465787949177,
      "total_volume": 1508047065791,
      "high_24h": 96770,
      "low_24h": 90302,
      "price_change_24h": 4774.85,
      "price_change_percentage_24h": 5.28456,
      "market_cap_change_24h": 585751309123,
      "market_cap_change_percentage_24h": 5.38373,
      "circulating_supply": 120521797.272525,
      "total_supply": 120521797.272525,
      "max_supply": null,
      "ath": 403838,
      "ath_change_percentage": -76.44238,
      "ath_date": "2022-03-07T16:44:57.811Z",
      "atl": 26.88,
      "atl_change_percentage": 353807.44995,
      "atl_date": "2015-10-20T00:00:00.000Z",
      "roi": {
        "times": 99.05149468737922,
        "currency": "btc",
        "percentage": 9905.149468737922
      },
      "last_updated": "2022-10-26T20:48:22.055Z"
    },
    {
      "id": "tether",
      "symbol": "usdt",
      "name": "Tether",
      "image": "https://assets.coingecko.com/coins/images/325/large/Tether-logo.png?1598003707",
      "current_price": 61.28,
      "market_cap": 4206858189933,
      "market_cap_rank": 3,
      "fully_diluted_valuation": 4206858189933,
      "total_volume": 4113983782166,
      "high_24h": 62.23,
      "low_24h": 60.94,
      "price_change_24h": -0.3693027350871958,
      "price_change_percentage_24h": -0.59899,
      "market_cap_change_24h": -18746254676.739746,
      "market_cap_change_percentage_24h": -0.44363,
      "circulating_supply": 68513908026.832,
      "total_supply": 68513908026.832,
      "max_supply": null,
      "ath": 155.26,
      "ath_change_percentage": -60.45297,
      "ath_date": "2022-03-07T17:56:57.160Z",
      "atl": 37.16,
      "atl_change_percentage": 65.25751,
      "atl_date": "2015-03-02T00:00:00.000Z",
      "roi": null,
      "last_updated": "2022-10-26T20:45:13.111Z"
    },
    {
      "id": "binancecoin",
      "symbol": "bnb",
      "name": "BNB",
      "image": "https://assets.coingecko.com/coins/images/825/large/bnb-icon2_2x.png?1644979850",
      "current_price": 17794.87,
      "market_cap": 2906118262264,
      "market_cap_rank": 4,
      "fully_diluted_valuation": 3559740458016,
      "total_volume": 64412767893,
      "high_24h": 17817.77,
      "low_24h": 17521.17,
      "price_change_24h": 129.58,
      "price_change_percentage_24h": 0.73351,
      "market_cap_change_24h": 23625000454,
      "market_cap_change_percentage_24h": 0.8196,
      "circulating_supply": 163276974.63,
      "total_supply": 163276974.63,
      "max_supply": 200000000,
      "ath": 58851,
      "ath_change_percentage": -69.75631,
      "ath_date": "2022-03-07T16:44:26.105Z",
      "atl": 2.28,
      "atl_change_percentage": 780325.00949,
      "atl_date": "2017-10-19T00:00:00.000Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:34.236Z"
    },
    {
      "id": "usd-coin",
      "symbol": "usdc",
      "name": "USD Coin",
      "image": "https://assets.coingecko.com/coins/images/6319/large/USD_Coin_icon.png?1547042389",
      "current_price": 61.33,
      "market_cap": 2690449259386,
      "market_cap_rank": 5,
      "fully_diluted_valuation": 2690449087106,
      "total_volume": 296051118958,
      "high_24h": 62.22,
      "low_24h": 60.71,
      "price_change_24h": -0.1764827875595003,
      "price_change_percentage_24h": -0.28695,
      "market_cap_change_24h": -16096391954.606445,
      "market_cap_change_percentage_24h": -0.59472,
      "circulating_supply": 43943587472.7166,
      "total_supply": 43943584658.8411,
      "max_supply": null,
      "ath": 155.25,
      "ath_change_percentage": -60.5602,
      "ath_date": "2022-03-07T17:44:50.584Z",
      "atl": 50.72,
      "atl_change_percentage": 20.71517,
      "atl_date": "2022-06-29T08:44:56.399Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:58.319Z"
    },
    {
      "id": "ripple",
      "symbol": "xrp",
      "name": "XRP",
      "image": "https://assets.coingecko.com/coins/images/44/large/xrp-symbol-white-128.png?1605778731",
      "current_price": 28.54,
      "market_cap": 1428085201847,
      "market_cap_rank": 6,
      "fully_diluted_valuation": 2851299975087,
      "total_volume": 96586589963,
      "high_24h": 28.78,
      "low_24h": 28.26,
      "price_change_24h": 0.217811,
      "price_change_percentage_24h": 0.76918,
      "market_cap_change_24h": 15269322445,
      "market_cap_change_percentage_24h": 1.08077,
      "circulating_supply": 50085407159,
      "total_supply": 99989240406,
      "max_supply": 100000000000,
      "ath": 193.62,
      "ath_change_percentage": -85.2729,
      "ath_date": "2018-01-07T00:00:00.000Z",
      "atl": 0.085527,
      "atl_change_percentage": 33239.54799,
      "atl_date": "2013-08-16T00:00:00.000Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:47.839Z"
    },
    {
      "id": "binance-usd",
      "symbol": "busd",
      "name": "Binance USD",
      "image": "https://assets.coingecko.com/coins/images/9576/large/BUSD.png?1568947766",
      "current_price": 61.33,
      "market_cap": 1315091639939,
      "market_cap_rank": 7,
      "fully_diluted_valuation": 1315091639939,
      "total_volume": 653787211194,
      "high_24h": 62.23,
      "low_24h": 61.03,
      "price_change_24h": -0.38098760842505186,
      "price_change_percentage_24h": -0.6174,
      "market_cap_change_24h": -17001981456.184326,
      "market_cap_change_percentage_24h": -1.27634,
      "circulating_supply": 21428575734.21,
      "total_supply": 21428575734.21,
      "max_supply": null,
      "ath": 155.5,
      "ath_change_percentage": -60.53775,
      "ath_date": "2022-03-07T17:54:06.922Z",
      "atl": 50.65,
      "atl_change_percentage": 21.14854,
      "atl_date": "2022-06-29T08:45:27.949Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:46.220Z"
    },
    {
      "id": "cardano",
      "symbol": "ada",
      "name": "Cardano",
      "image": "https://assets.coingecko.com/coins/images/975/large/cardano.png?1547034860",
      "current_price": 24.7,
      "market_cap": 865531474159,
      "market_cap_rank": 8,
      "fully_diluted_valuation": 1111396581150,
      "total_volume": 53656629723,
      "high_24h": 25.41,
      "low_24h": 24.46,
      "price_change_24h": -0.20478801084039233,
      "price_change_percentage_24h": -0.82224,
      "market_cap_change_24h": -9225066371.28003,
      "market_cap_change_percentage_24h": -1.05459,
      "circulating_supply": 35045020830.3234,
      "total_supply": 45000000000,
      "max_supply": 45000000000,
      "ath": 225.39,
      "ath_change_percentage": -89.04234,
      "ath_date": "2021-09-02T06:00:10.474Z",
      "atl": 1.24,
      "atl_change_percentage": 1887.39248,
      "atl_date": "2017-11-02T00:00:00.000Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:38.497Z"
    },
    {
      "id": "solana",
      "symbol": "sol",
      "name": "Solana",
      "image": "https://assets.coingecko.com/coins/images/4128/large/solana.png?1640133422",
      "current_price": 1913.14,
      "market_cap": 685250345788,
      "market_cap_rank": 9,
      "fully_diluted_valuation": null,
      "total_volume": 77587099273,
      "high_24h": 1944.56,
      "low_24h": 1885.86,
      "price_change_24h": 9.27,
      "price_change_percentage_24h": 0.48696,
      "market_cap_change_24h": 2991248362,
      "market_cap_change_percentage_24h": 0.43843,
      "circulating_supply": 358516199.419909,
      "total_supply": 531974095.027108,
      "max_supply": null,
      "ath": 18495.72,
      "ath_change_percentage": -89.66475,
      "ath_date": "2021-11-06T21:54:35.825Z",
      "atl": 36.89,
      "atl_change_percentage": 5082.24017,
      "atl_date": "2020-05-11T19:35:23.449Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:29.845Z"
    },
    {
      "id": "dogecoin",
      "symbol": "doge",
      "name": "Dogecoin",
      "image": "https://assets.coingecko.com/coins/images/5/large/dogecoin.png?1547792256",
      "current_price": 4.43,
      "market_cap": 603890115368,
      "market_cap_rank": 10,
      "fully_diluted_valuation": null,
      "total_volume": 80086375394,
      "high_24h": 4.47,
      "low_24h": 3.86,
      "price_change_24h": 0.573418,
      "price_change_percentage_24h": 14.87394,
      "market_cap_change_24h": 76688680424,
      "market_cap_change_percentage_24h": 14.54637,
      "circulating_supply": 136644236383.705,
      "total_supply": null,
      "max_supply": null,
      "ath": 53.93,
      "ath_change_percentage": -91.80544,
      "ath_date": "2021-05-08T05:08:23.458Z",
      "atl": 0.00382859,
      "atl_change_percentage": 115332.49013,
      "atl_date": "2014-08-18T00:00:00.000Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:37.544Z"
    },
    {
      "id": "matic-network",
      "symbol": "matic",
      "name": "Polygon",
      "image": "https://assets.coingecko.com/coins/images/4713/large/matic-token-icon.png?1624446912",
      "current_price": 57.15,
      "market_cap": 505827004085,
      "market_cap_rank": 11,
      "fully_diluted_valuation": 570991997362,
      "total_volume": 40663978986,
      "high_24h": 59.22,
      "low_24h": 56.46,
      "price_change_24h": 0.684041,
      "price_change_percentage_24h": 1.21149,
      "market_cap_change_24h": 85795043892,
      "market_cap_change_percentage_24h": 20.42584,
      "circulating_supply": 8858740690.28493,
      "total_supply": 10000000000,
      "max_supply": 10000000000,
      "ath": 227.25,
      "ath_change_percentage": -74.87991,
      "ath_date": "2022-03-07T16:44:57.800Z",
      "atl": 0.20509,
      "atl_change_percentage": 27734.331,
      "atl_date": "2019-05-10T00:00:00.000Z",
      "roi": {
        "times": 353.61246271321613,
        "currency": "usd",
        "percentage": 35361.246271321615
      },
      "last_updated": "2022-10-26T20:48:52.428Z"
    },
    {
      "id": "polkadot",
      "symbol": "dot",
      "name": "Polkadot",
      "image": "https://assets.coingecko.com/coins/images/12171/large/polkadot.png?1639712644",
      "current_price": 395.61,
      "market_cap": 460905603819,
      "market_cap_rank": 12,
      "fully_diluted_valuation": 492929929523,
      "total_volume": 20199371951,
      "high_24h": 404.31,
      "low_24h": 393.1,
      "price_change_24h": -2.000018345758008,
      "price_change_percentage_24h": -0.50301,
      "market_cap_change_24h": -3244866722.661499,
      "market_cap_change_percentage_24h": -0.6991,
      "circulating_supply": 1165048996.39147,
      "total_supply": 1245998128.30132,
      "max_supply": null,
      "ath": 3945.69,
      "ath_change_percentage": -89.97647,
      "ath_date": "2021-11-03T18:54:43.566Z",
      "atl": 197.86,
      "atl_change_percentage": 99.89135,
      "atl_date": "2020-08-20T05:48:11.359Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:42.406Z"
    },
    {
      "id": "staked-ether",
      "symbol": "steth",
      "name": "Lido Staked Ether",
      "image": "https://assets.coingecko.com/coins/images/13442/large/steth_logo.png?1608607546",
      "current_price": 94958,
      "market_cap": 429179758596,
      "market_cap_rank": 13,
      "fully_diluted_valuation": 429179758596,
      "total_volume": 1619790320,
      "high_24h": 96615,
      "low_24h": 90120,
      "price_change_24h": 4689.31,
      "price_change_percentage_24h": 5.19485,
      "market_cap_change_24h": 25162668981,
      "market_cap_change_percentage_24h": 6.22812,
      "circulating_supply": 4518686.06201948,
      "total_supply": 4518686.06201948,
      "max_supply": 4518686.06201948,
      "ath": 401469,
      "ath_change_percentage": -76.37608,
      "ath_date": "2022-03-07T16:20:48.290Z",
      "atl": 36164,
      "atl_change_percentage": 162.25478,
      "atl_date": "2020-12-22T04:08:21.854Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:55.662Z"
    },
    {
      "id": "shiba-inu",
      "symbol": "shib",
      "name": "Shiba Inu",
      "image": "https://assets.coingecko.com/coins/images/11939/large/shiba.png?1622619446",
      "current_price": 0.00065328,
      "market_cap": 385094060829,
      "market_cap_rank": 14,
      "fully_diluted_valuation": null,
      "total_volume": 25565594561,
      "high_24h": 0.00065713,
      "low_24h": 0.00062667,
      "price_change_24h": 0.00002661,
      "price_change_percentage_24h": 4.24602,
      "market_cap_change_24h": 15642401137,
      "market_cap_change_percentage_24h": 4.23395,
      "circulating_supply": 589372889898258.2,
      "total_supply": 999991083835966,
      "max_supply": null,
      "ath": 0.0060834,
      "ath_change_percentage": -89.27605,
      "ath_date": "2021-10-28T03:59:39.944Z",
      "atl": 4.167e-9,
      "atl_change_percentage": 15657292.91875,
      "atl_date": "2020-12-11T19:13:27.875Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:50.258Z"
    },
    {
      "id": "tron",
      "symbol": "trx",
      "name": "TRON",
      "image": "https://assets.coingecko.com/coins/images/1094/large/tron-logo.png?1547035066",
      "current_price": 3.88,
      "market_cap": 357938045450,
      "market_cap_rank": 15,
      "fully_diluted_valuation": 357938000309,
      "total_volume": 18731972080,
      "high_24h": 3.91,
      "low_24h": 3.83,
      "price_change_24h": 0.04754478,
      "price_change_percentage_24h": 1.23944,
      "market_cap_change_24h": 3386919059,
      "market_cap_change_percentage_24h": 0.95527,
      "circulating_supply": 92277194840.0455,
      "total_supply": 92277183202.5591,
      "max_supply": null,
      "ath": 13.46,
      "ath_change_percentage": -71.17457,
      "ath_date": "2021-04-17T03:43:18.701Z",
      "atl": 0.10688,
      "atl_change_percentage": 3529.72825,
      "atl_date": "2017-11-12T00:00:00.000Z",
      "roi": {
        "times": 32.35729759505246,
        "currency": "usd",
        "percentage": 3235.729759505246
      },
      "last_updated": "2022-10-26T20:48:36.241Z"
    },
    {
      "id": "dai",
      "symbol": "dai",
      "name": "Dai",
      "image": "https://assets.coingecko.com/coins/images/9956/large/4943.png?1636636734",
      "current_price": 61.29,
      "market_cap": 354524449255,
      "market_cap_rank": 16,
      "fully_diluted_valuation": 354524449255,
      "total_volume": 25632736999,
      "high_24h": 62.14,
      "low_24h": 60.98,
      "price_change_24h": -0.44064532314624927,
      "price_change_percentage_24h": -0.71386,
      "market_cap_change_24h": -2431004766.6969604,
      "market_cap_change_percentage_24h": -0.68104,
      "circulating_supply": 5782951329.74095,
      "total_supply": 5782951329.74095,
      "max_supply": 5782951329.74095,
      "ath": 155.2,
      "ath_change_percentage": -60.50678,
      "ath_date": "2022-03-07T17:46:55.816Z",
      "atl": 50.72,
      "atl_change_percentage": 20.85032,
      "atl_date": "2022-06-29T08:41:18.364Z",
      "roi": null,
      "last_updated": "2022-10-26T20:45:37.271Z"
    },
    {
      "id": "wrapped-bitcoin",
      "symbol": "wbtc",
      "name": "Wrapped Bitcoin",
      "image": "https://assets.coingecko.com/coins/images/7598/large/wrapped_bitcoin_wbtc.png?1548822744",
      "current_price": 1273290,
      "market_cap": 311132167149,
      "market_cap_rank": 17,
      "fully_diluted_valuation": 311132167149,
      "total_volume": 21288909001,
      "high_24h": 1283191,
      "low_24h": 1238466,
      "price_change_24h": 31441,
      "price_change_percentage_24h": 2.53177,
      "market_cap_change_24h": 7183219495,
      "market_cap_change_percentage_24h": 2.3633,
      "circulating_supply": 244880.45135981,
      "total_supply": 244880.45135981,
      "max_supply": 244880.45135981,
      "ath": 6054520,
      "ath_change_percentage": -79.01324,
      "ath_date": "2022-03-07T16:44:38.852Z",
      "atl": 204797,
      "atl_change_percentage": 520.44114,
      "atl_date": "2019-04-02T00:00:00.000Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:44.695Z"
    },
    {
      "id": "uniswap",
      "symbol": "uni",
      "name": "Uniswap",
      "image": "https://assets.coingecko.com/coins/images/12504/large/uniswap-uni.png?1600306604",
      "current_price": 412.35,
      "market_cap": 310449350774,
      "market_cap_rank": 18,
      "fully_diluted_valuation": 411863995008,
      "total_volume": 9893196967,
      "high_24h": 420.45,
      "low_24h": 403.75,
      "price_change_24h": 8.58,
      "price_change_percentage_24h": 2.12512,
      "market_cap_change_24h": 5491946759,
      "market_cap_change_percentage_24h": 1.80089,
      "circulating_supply": 753766667,
      "total_supply": 1000000000,
      "max_supply": 1000000000,
      "ath": 3385.48,
      "ath_change_percentage": -87.8483,
      "ath_date": "2021-05-03T07:48:59.347Z",
      "atl": 77.17,
      "atl_change_percentage": 433.08906,
      "atl_date": "2020-09-17T01:20:38.214Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:35.605Z"
    },
    {
      "id": "avalanche-2",
      "symbol": "avax",
      "name": "Avalanche",
      "image": "https://assets.coingecko.com/coins/images/12559/large/coin-round-red.png?1604021818",
      "current_price": 1041.5,
      "market_cap": 309925079293,
      "market_cap_rank": 19,
      "fully_diluted_valuation": 749414518229,
      "total_volume": 19991959703,
      "high_24h": 1060.6,
      "low_24h": 1016.93,
      "price_change_24h": 24.57,
      "price_change_percentage_24h": 2.41587,
      "market_cap_change_24h": 7159117571,
      "market_cap_change_percentage_24h": 2.36457,
      "circulating_supply": 297760520.597514,
      "total_supply": 412509802.810158,
      "max_supply": 720000000,
      "ath": 11648.52,
      "ath_change_percentage": -91.0768,
      "ath_date": "2022-03-07T17:54:44.523Z",
      "atl": 205.96,
      "atl_change_percentage": 404.68272,
      "atl_date": "2020-12-09T08:34:53.550Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:49.434Z"
    },
    {
      "id": "okb",
      "symbol": "okb",
      "name": "OKB",
      "image": "https://assets.coingecko.com/coins/images/4463/large/WeChat_Image_20220118095654.png?1642471050",
      "current_price": 990.26,
      "market_cap": 249577232099,
      "market_cap_rank": 20,
      "fully_diluted_valuation": null,
      "total_volume": 1957587032,
      "high_24h": 1007.42,
      "low_24h": 979.33,
      "price_change_24h": 8.1,
      "price_change_percentage_24h": 0.82443,
      "market_cap_change_24h": 1511321007,
      "market_cap_change_percentage_24h": 0.60924,
      "circulating_supply": 251627611.56,
      "total_supply": 300000000,
      "max_supply": null,
      "ath": 3310.29,
      "ath_change_percentage": -70.03728,
      "ath_date": "2021-05-03T01:03:16.108Z",
      "atl": 38.31,
      "atl_change_percentage": 2489.10803,
      "atl_date": "2019-02-01T00:00:00.000Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:47.715Z"
    },
    {
      "id": "leo-token",
      "symbol": "leo",
      "name": "LEO Token",
      "image": "https://assets.coingecko.com/coins/images/8418/large/leo-token.png?1558326215",
      "current_price": 264.75,
      "market_cap": 247425532664,
      "market_cap_rank": 21,
      "fully_diluted_valuation": null,
      "total_volume": 77114162,
      "high_24h": 265.57,
      "low_24h": 254.27,
      "price_change_24h": 10.48,
      "price_change_percentage_24h": 4.12249,
      "market_cap_change_24h": 9043943621,
      "market_cap_change_percentage_24h": 3.79389,
      "circulating_supply": 933582666.9,
      "total_supply": 985239504,
      "max_supply": null,
      "ath": 855.14,
      "ath_change_percentage": -69.00689,
      "ath_date": "2022-03-07T17:44:57.294Z",
      "atl": 49.56,
      "atl_change_percentage": 434.73138,
      "atl_date": "2019-12-24T15:14:35.376Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:48.115Z"
    },
    {
      "id": "litecoin",
      "symbol": "ltc",
      "name": "Litecoin",
      "image": "https://assets.coingecko.com/coins/images/2/large/litecoin.png?1547033580",
      "current_price": 3433.59,
      "market_cap": 245353659147,
      "market_cap_rank": 22,
      "fully_diluted_valuation": 288355604413,
      "total_volume": 27707894393,
      "high_24h": 3523.3,
      "low_24h": 3410.58,
      "price_change_24h": -19.30514610828004,
      "price_change_percentage_24h": -0.5591,
      "market_cap_change_24h": -1779506792.6321106,
      "market_cap_change_percentage_24h": -0.72006,
      "circulating_supply": 71473233.2334713,
      "total_supply": 84000000,
      "max_supply": 84000000,
      "ath": 30247,
      "ath_change_percentage": -88.64964,
      "ath_date": "2021-05-10T03:13:07.904Z",
      "atl": 51.1,
      "atl_change_percentage": 6618.50297,
      "atl_date": "2013-10-22T00:00:00.000Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:41.771Z"
    },
    {
      "id": "cosmos",
      "symbol": "atom",
      "name": "Cosmos Hub",
      "image": "https://assets.coingecko.com/coins/images/1481/large/cosmos_hub.png?1555657960",
      "current_price": 748.25,
      "market_cap": 218927797655,
      "market_cap_rank": 23,
      "fully_diluted_valuation": null,
      "total_volume": 16511122289,
      "high_24h": 763.84,
      "low_24h": 737.39,
      "price_change_24h": 10.86,
      "price_change_percentage_24h": 1.47325,
      "market_cap_change_24h": 2870363393,
      "market_cap_change_percentage_24h": 1.32852,
      "circulating_supply": 292586163.827428,
      "total_supply": null,
      "max_supply": null,
      "ath": 4556.15,
      "ath_change_percentage": -83.57712,
      "ath_date": "2022-03-07T17:20:25.124Z",
      "atl": 86.9,
      "atl_change_percentage": 761.04326,
      "atl_date": "2020-03-13T02:27:44.591Z",
      "roi": {
        "times": 121.1138575040391,
        "currency": "usd",
        "percentage": 12111.38575040391
      },
      "last_updated": "2022-10-26T20:48:34.152Z"
    },
    {
      "id": "chainlink",
      "symbol": "link",
      "name": "Chainlink",
      "image": "https://assets.coingecko.com/coins/images/877/large/chainlink-new-logo.png?1547034700",
      "current_price": 437.5,
      "market_cap": 215099557926,
      "market_cap_rank": 24,
      "fully_diluted_valuation": 437549980703,
      "total_volume": 23462372122,
      "high_24h": 445.73,
      "low_24h": 432.82,
      "price_change_24h": 3.8,
      "price_change_percentage_24h": 0.8762,
      "market_cap_change_24h": 1896351982,
      "market_cap_change_percentage_24h": 0.88946,
      "circulating_supply": 491599971.2305644,
      "total_supply": 1000000000,
      "max_supply": 1000000000,
      "ath": 3883.64,
      "ath_change_percentage": -88.73352,
      "ath_date": "2021-05-10T00:13:57.214Z",
      "atl": 8.69,
      "atl_change_percentage": 4935.78116,
      "atl_date": "2017-11-29T00:00:00.000Z",
      "roi": null,
      "last_updated": "2022-10-26T20:48:40.379Z"
    },
    {
      "id": "ethereum-classic",
      "symbol": "etc",
      "name": "Ethereum Classic",
      "image": "https://assets.coingecko.com/coins/images/453/large/ethereum-classic-logo.png?1547034169",
      "current_price": 1555.01,
      "market_cap": 213950822773,
      "market_cap_rank": 25,
      "fully_diluted_valuation": 327671221441,
      "total_volume": 36495010576,
      "high_24h": 1589.83,
      "low_24h": 1522.04,
      "price_change_24h": 31.06,
      "price_change_percentage_24h": 2.03801,
      "market_cap_change_24h": 3708024375,
      "market_cap_change_percentage_24h": 1.76369,
      "circulating_supply": 137575213.837881,
      "total_supply": 210700000,
      "max_supply": 210700000,
      "ath": 12414.52,
      "ath_change_percentage": -87.47309,
      "ath_date": "2021-05-06T18:34:22.133Z",
      "atl": 40.06,
      "atl_change_percentage": 3782.37577,
      "atl_date": "2016-07-25T00:00:00.000Z",
      "roi": {
        "times": 55.39469830475647,
        "currency": "usd",
        "percentage": 5539.469830475647
      },
      "last_updated": "2022-10-26T20:48:46.534Z"
    }
  ],
  "charts": [
    {
      "id": "bitcoin",
      "prices": [
        [
          "30.10.2022",
          1279763.5243729677
        ],
        [
          "31.10.2022",
          1268058.7596194344
        ],
        [
          "01.11.2022",
          1267078.596830569
        ],
        [
          "02.11.2022",
          1265233.7475080818
        ],
        [
          "03.11.2022",
          1249094.691081628
        ],
        [
          "04.11.2022",
          1260150.4902614513
        ],
        [
          "05.11.2022",
          1311319.671954146
        ]
      ]
    },
    {
      "id": "ethereum",
      "prices": [
        [
          "30.10.2022",
          99635.40675212638
        ],
        [
          "31.10.2022",
          97825.81988445956
        ],
        [
          "01.11.2022",
          97249.44906994817
        ],
        [
          "02.11.2022",
          97588.23981471396
        ],
        [
          "03.11.2022",
          94203.39765071847
        ],
        [
          "04.11.2022",
          95464.88018230018
        ],
        [
          "05.11.2022",
          101939.96540511878
        ]
      ]
    },
    {
      "id": "tether",
      "prices": [
        [
          "30.10.2022",
          61.521813223005104
        ],
        [
          "31.10.2022",
          61.48825308074678
        ],
        [
          "01.11.2022",
          61.811046660498114
        ],
        [
          "02.11.2022",
          61.76502999845441
        ],
        [
          "03.11.2022",
          61.978263790318
        ],
        [
          "04.11.2022",
          62.37460946196816
        ],
        [
          "05.11.2022",
          61.994909110869564
        ]
      ]
    },
    {
      "id": "binancecoin",
      "prices": [
        [
          "30.10.2022",
          18682.53070078313
        ],
        [
          "31.10.2022",
          19281.730794327155
        ],
        [
          "01.11.2022",
          20174.824566568474
        ],
        [
          "02.11.2022",
          20049.835235504434
        ],
        [
          "03.11.2022",
          19840.162011801713
        ],
        [
          "04.11.2022",
          20549.60388918379
        ],
        [
          "05.11.2022",
          21882.663554750852
        ]
      ]
    },
    {
      "id": "usd-coin",
      "prices": [
        [
          "30.10.2022",
          61.482353605219174
        ],
        [
          "31.10.2022",
          61.47048509090562
        ],
        [
          "01.11.2022",
          61.80840882668916
        ],
        [
          "02.11.2022",
          61.80499904824047
        ],
        [
          "03.11.2022",
          61.947652102988435
        ],
        [
          "04.11.2022",
          62.37018994285825
        ],
        [
          "05.11.2022",
          62.01059347328931
        ]
      ]
    },
    {
      "id": "ripple",
      "prices": [
        [
          "30.10.2022",
          28.84075234725443
        ],
        [
          "31.10.2022",
          28.129665841060127
        ],
        [
          "01.11.2022",
          28.74970242354824
        ],
        [
          "02.11.2022",
          28.66880875338195
        ],
        [
          "03.11.2022",
          27.963120155130675
        ],
        [
          "04.11.2022",
          28.375700600793127
        ],
        [
          "05.11.2022",
          31.127583139306964
        ]
      ]
    },
    {
      "id": "binance-usd",
      "prices": [
        [
          "30.10.2022",
          61.5104370609021
        ],
        [
          "31.10.2022",
          61.49340392065531
        ],
        [
          "01.11.2022",
          61.82894706069786
        ],
        [
          "02.11.2022",
          61.77718642193757
        ],
        [
          "03.11.2022",
          61.98885479172991
        ],
        [
          "04.11.2022",
          62.38143939725206
        ],
        [
          "05.11.2022",
          61.95354040515704
        ]
      ]
    },
    {
      "id": "cardano",
      "prices": [
        [
          "30.10.2022",
          25.729772139789805
        ],
        [
          "31.10.2022",
          24.920387671411515
        ],
        [
          "01.11.2022",
          25.110878296695784
        ],
        [
          "02.11.2022",
          24.766530004488757
        ],
        [
          "03.11.2022",
          23.925731685482113
        ],
        [
          "04.11.2022",
          24.272249313870425
        ],
        [
          "05.11.2022",
          26.13449714892618
        ]
      ]
    },
    {
      "id": "solana",
      "prices": [
        [
          "30.10.2022",
          2020.4470094875653
        ],
        [
          "31.10.2022",
          2023.2984967687091
        ],
        [
          "01.11.2022",
          2015.5732841253564
        ],
        [
          "02.11.2022",
          1990.8794410600515
        ],
        [
          "03.11.2022",
          1907.3364148587177
        ],
        [
          "04.11.2022",
          1922.038691445992
        ],
        [
          "05.11.2022",
          2094.8829566751087
        ]
      ]
    },
    {
      "id": "dogecoin",
      "prices": [
        [
          "30.10.2022",
          7.380302497162907
        ],
        [
          "31.10.2022",
          7.228495282713911
        ],
        [
          "01.11.2022",
          7.837449058547694
        ],
        [
          "02.11.2022",
          8.799244832844035
        ],
        [
          "03.11.2022",
          7.922372884564317
        ],
        [
          "04.11.2022",
          7.6370113256587695
        ],
        [
          "05.11.2022",
          7.811851060483124
        ]
      ]
    },
    {
      "id": "matic-network",
      "prices": [
        [
          "30.10.2022",
          57.438380995200276
        ],
        [
          "31.10.2022",
          55.83913010702376
        ],
        [
          "01.11.2022",
          55.840930222787954
        ],
        [
          "02.11.2022",
          54.04253627971138
        ],
        [
          "03.11.2022",
          54.0515647716764
        ],
        [
          "04.11.2022",
          59.40016448530504
        ],
        [
          "05.11.2022",
          72.43417719579261
        ]
      ]
    },
    {
      "id": "polkadot",
      "prices": [
        [
          "30.10.2022",
          407.8254142121601
        ],
        [
          "31.10.2022",
          408.68501783936046
        ],
        [
          "01.11.2022",
          409.88496379413203
        ],
        [
          "02.11.2022",
          399.5786652351322
        ],
        [
          "03.11.2022",
          387.06627904864325
        ],
        [
          "04.11.2022",
          400.3476695105826
        ],
        [
          "05.11.2022",
          438.38143988111074
        ]
      ]
    },
    {
      "id": "staked-ether",
      "prices": [
        [
          "30.10.2022",
          99551.63886944683
        ],
        [
          "31.10.2022",
          97677.42649558869
        ],
        [
          "01.11.2022",
          97226.72273619712
        ],
        [
          "02.11.2022",
          97532.8330258558
        ],
        [
          "03.11.2022",
          94185.09886987
        ],
        [
          "04.11.2022",
          95357.62669388037
        ],
        [
          "05.11.2022",
          101861.49971488601
        ]
      ]
    },
    {
      "id": "shiba-inu",
      "prices": [
        [
          "30.10.2022",
          0.0007874894691138442
        ],
        [
          "31.10.2022",
          0.0007341113271794481
        ],
        [
          "01.11.2022",
          0.0007715305919527699
        ],
        [
          "02.11.2022",
          0.0007948467019800995
        ],
        [
          "03.11.2022",
          0.0007297198738180641
        ],
        [
          "04.11.2022",
          0.0007308426326654089
        ],
        [
          "05.11.2022",
          0.0007767094518423622
        ]
      ]
    },
    {
      "id": "tron",
      "prices": [
        [
          "30.10.2022",
          3.9314899378391646
        ],
        [
          "31.10.2022",
          3.879162291182431
        ],
        [
          "01.11.2022",
          3.916643312031191
        ],
        [
          "02.11.2022",
          3.8814080412216008
        ],
        [
          "03.11.2022",
          3.8150006204404865
        ],
        [
          "04.11.2022",
          3.851280192957097
        ],
        [
          "05.11.2022",
          3.948664526259157
        ]
      ]
    },
    {
      "id": "dai",
      "prices": [
        [
          "30.10.2022",
          61.477921324972144
        ],
        [
          "31.10.2022",
          61.45893247857486
        ],
        [
          "01.11.2022",
          61.83505546174872
        ],
        [
          "02.11.2022",
          61.700932471024515
        ],
        [
          "03.11.2022",
          61.98941230825281
        ],
        [
          "04.11.2022",
          62.38012101325344
        ],
        [
          "05.11.2022",
          61.98741865331954
        ]
      ]
    },
    {
      "id": "wrapped-bitcoin",
      "prices": [
        [
          "30.10.2022",
          1282390.8626911808
        ],
        [
          "31.10.2022",
          1266652.6567777828
        ],
        [
          "01.11.2022",
          1265754.4551896695
        ],
        [
          "02.11.2022",
          1264464.1375775717
        ],
        [
          "03.11.2022",
          1248723.6500189311
        ],
        [
          "04.11.2022",
          1260120.356392855
        ],
        [
          "05.11.2022",
          1311650.2481142916
        ]
      ]
    },
    {
      "id": "uniswap",
      "prices": [
        [
          "30.10.2022",
          434.99704141495954
        ],
        [
          "31.10.2022",
          424.25642083029726
        ],
        [
          "01.11.2022",
          431.1221995108025
        ],
        [
          "02.11.2022",
          440.081798013608
        ],
        [
          "03.11.2022",
          439.7050387162852
        ],
        [
          "04.11.2022",
          432.19929483182113
        ],
        [
          "05.11.2022",
          467.287282600435
        ]
      ]
    },
    {
      "id": "avalanche-2",
      "prices": [
        [
          "30.10.2022",
          1125.7184344293075
        ],
        [
          "31.10.2022",
          1122.028917761602
        ],
        [
          "01.11.2022",
          1193.0745071849199
        ],
        [
          "02.11.2022",
          1152.4875749980104
        ],
        [
          "03.11.2022",
          1109.23052128535
        ],
        [
          "04.11.2022",
          1124.3770942099045
        ],
        [
          "05.11.2022",
          1201.1675939961458
        ]
      ]
    },
    {
      "id": "okb",
      "prices": [
        [
          "30.10.2022",
          996.1007909201293
        ],
        [
          "31.10.2022",
          993.3064275568223
        ],
        [
          "01.11.2022",
          1061.909382605641
        ],
        [
          "02.11.2022",
          1014.3450889299065
        ],
        [
          "03.11.2022",
          998.4807113345864
        ],
        [
          "04.11.2022",
          1244.1439756459229
        ],
        [
          "05.11.2022",
          1276.6405270704697
        ]
      ]
    },
    {
      "id": "leo-token",
      "prices": [
        [
          "30.10.2022",
          275.75873224025986
        ],
        [
          "31.10.2022",
          276.7147447906376
        ],
        [
          "01.11.2022",
          280.74093293018075
        ],
        [
          "02.11.2022",
          280.9447852526161
        ],
        [
          "03.11.2022",
          289.5757647198543
        ],
        [
          "04.11.2022",
          292.7956987944186
        ],
        [
          "05.11.2022",
          265.76386272368103
        ]
      ]
    },
    {
      "id": "litecoin",
      "prices": [
        [
          "30.10.2022",
          3472.9920350041734
        ],
        [
          "31.10.2022",
          3404.7582739345353
        ],
        [
          "01.11.2022",
          3404.9677189188337
        ],
        [
          "02.11.2022",
          3404.611715892163
        ],
        [
          "03.11.2022",
          3743.6097764723177
        ],
        [
          "04.11.2022",
          3864.2884805046824
        ],
        [
          "05.11.2022",
          4189.017734888164
        ]
      ]
    },
    {
      "id": "cosmos",
      "prices": [
        [
          "30.10.2022",
          827.3457113316763
        ],
        [
          "31.10.2022",
          856.4066821054571
        ],
        [
          "01.11.2022",
          884.6420069861247
        ],
        [
          "02.11.2022",
          871.7006262481993
        ],
        [
          "03.11.2022",
          824.4681899051354
        ],
        [
          "04.11.2022",
          841.0536477578398
        ],
        [
          "05.11.2022",
          932.2151606020898
        ]
      ]
    },
    {
      "id": "chainlink",
      "prices": [
        [
          "30.10.2022",
          466.65417983388704
        ],
        [
          "31.10.2022",
          478.38160533095413
        ],
        [
          "01.11.2022",
          485.87843315102725
        ],
        [
          "02.11.2022",
          475.2269932495643
        ],
        [
          "03.11.2022",
          460.4771012732639
        ],
        [
          "04.11.2022",
          480.26854857741984
        ],
        [
          "05.11.2022",
          542.3991193197472
        ]
      ]
    },
    {
      "id": "ethereum-classic",
      "prices": [
        [
          "30.10.2022",
          1586.5693151625787
        ],
        [
          "31.10.2022",
          1505.0637148659234
        ],
        [
          "01.11.2022",
          1498.5845545221894
        ],
        [
          "02.11.2022",
          1484.8329337359867
        ],
        [
          "03.11.2022",
          1420.9707530697913
        ],
        [
          "04.11.2022",
          1495.3169103408586
        ],
        [
          "05.11.2022",
          1596.01347308772
        ]
      ]
    }
  ]
}```

* `users.js`
```python
import {usersAPI} from "@/api";
import {defineStore} from "pinia"
import router from "@/router";


const useUsersStore = defineStore('users', {
    state: () => ({
        user: {
            id: null,
            coins: []
        }
    }),

    actions: {
        async signUp(credentials) {
            const response = await usersAPI.getAllUsers()
            const data = response.data

            const validUser = this.isValid(credentials, data)

            if (validUser !== undefined) {
                this.user.id = validUser.id;
                this.user.coins = validUser.coins;
                await router.push('/personal')
            } else {
                localStorage.clear()
                alert('Ошибка! Проверьте email или пароль')
            }
        },

        isValid(credentials, data) {
            for (let i = 0; i < data.length; i++) {
                if (data[i].email === credentials.email && data[i].password === credentials.password) {
                    return {id: data[i].id, coins: data[i].coins}
                }
            }
        },

        async commitActions(user) {
            const rawUser = JSON.parse(JSON.stringify(user))
            const currentUser = await usersAPI.getCurrentUser(rawUser.id)
            currentUser.data.coins = rawUser.coins
            const response = await usersAPI.push(currentUser.data)
            return response.data
        },

        async register(credentials) {
            const response = await usersAPI.createNewUser(credentials)
            const data = response.data

            let {id} = data

            this.user = {
                'id': id,
                'coins': [],
            }
        }
    }
})

export default useUsersStore```

* `Personal.vue`
```python
<template>
  <section class="dataTable-wrapper">
    <div class="dataTable-wrapper d-flex justify-content-center">
      <table class="table align-middle border-light mt-5 w-75">
        <tr class="head-row border-light ">
          <th class="align-middle fw-bold">Название
<!--            <sort-button/>-->
          </th>
          <th class="align-middle fw-bold">Цена
<!--            <sort-button/>-->
          </th>
          <th class="fw-bold">Количество
<!--            <sort-button/>-->
          </th>
          <th class="fw-bold">Итого</th>
          <th class="fw-normal">
            <div class="">
              <select-sort
                  v-model="sortName"
                  :options="sortOptions"
              />
            </div>
          </th>
          <th class="d-flex justify-content-center">
            <div>
              <p class="balance m-0">Баланс:</p>
              <p class="balance fw-light m-0">{{ balance() }}
              </p>
            </div>
          </th>
        </tr>
        <wallet :coins="coins" @buyEvent="buyCoin" @sellEvent="sellCoin"/>
      </table>
    </div>
  </section>
</template>

<script>
import Wallet from "@/components/lists/Wallet.vue";
import {mapActions, mapState} from "pinia";
import useCoinsStore from "@/stores/coins";
import useUsersStore from "@/stores/users";

export default {
  name: 'Personal',
  components: {
    Wallet
  },
  data() {
    return {
      coins: [],
      sortName: '',
      sortOptions: [
        {value: 'name ASC', name: 'По названию (ASC)'},
        {value: 'name DESC', name: 'По названию (DESC)'},
        {value: 'current_price ASC', name: 'По цене (ASC)'},
        {value: 'current_price DESC', name: 'По цене (DESC)'},
        {value: 'amount ASC', name: 'По количеству (ASC)'},
        {value: 'amount DESC', name: 'По количеству (DESC)'},
      ]
    }
  },
  methods: {
    ...mapActions(useCoinsStore, ['getWallet', "loadCoins", "loadCustomCoins"]),
    ...mapActions(useUsersStore, ['commitActions']),

    async getCoins() {
      let current = await this.getWallet(this.user.id);
      const data = await this.loadCustomCoins()
      for (let i = 0; i < current.coins.length; i++) {
        for (let j = 0; j < data.length; j++) {
          if (current.coins[i].id === data[j].id) {
            this.coins[i] = data[j]
            this.coins[i].amount = current.coins[i].amount
          }
        }
      }
    },

    balance() {
      let res = 0;
      for (let i = 0; i < this.coins.length; i++) {
        res += this.coins[i].amount * this.coins[i].current_price;
      }
      return res.toFixed(2)
    },

    async buyCoin(id, amount) {
      let newCoin = true
      for (let i = 0; i < this.user.coins.length; i++) {
        if (id === this.user.coins[i].id) {
          this.user.coins[i].amount += amount
          newCoin = false
        }
      }

      if (newCoin) {
        this.user.coins.push({id: id, amount: amount})
      }

      await this.commitActions(this.user);
      await this.getCoins()
    },

    async sellCoin(id, amount) {
      let index;
      for (let i = 0; i < this.user.coins.length; i++) {
        if (id === this.user.coins[i].id) {
          this.user.coins[i].amount -= amount;
          index = i;
        }
      }

      if (this.user.coins[index].amount === 0) {
        this.user.coins = this.user.coins.filter(coin => coin.id !== id)
      }

      await this.commitActions(this.user);
      await this.getCoins()
      location.reload()
    }
  },
  computed: {
    ...mapState(useUsersStore, ['user'])
  },
  mounted() {
    this.getCoins()
  },
  watch: {
    async sortName(sortName) {
      const sortSplit = sortName.split(' ')
      const type = sortSplit[0]
      const order = sortSplit[1]
      if (type === 'name') {
        this.coins.sort((a, b) => a[type].localeCompare(b[type]))
      } else {
        this.coins.sort((a, b) => a[type] - b[type])
      }
      if (order === 'DESC') {
        this.coins.reverse()
      }
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Tahoma', sans-serif
}

.table {
  border: 2px solid;
}

.head-row {
  border-bottom: 2px solid;
  font-weight: normal;
}

.head-row {
  font-weight: normal;
}

.table thead th {
  padding: 30px;
  font-weight: normal;
}

.dataTable-wrapper {
  margin: 20px auto;
  overflow-x: auto
}


::placeholder {
  color: black;
  font-weight: 600;
}


.table tbody td {
  padding: 30px;
  margin: 0;
}

.btn-pagination {
  border: none;
  background-color: white;
  margin-left: 15px;
}


body {
  background-color: var(--bg-color) !important;
  color: var(--text-color) !important;
  border-color: var(--card-color) !important;
}

.page-number {
  border-color: var(--text-color);
}

tr {
  border-color: var(--card-color) !important;
}
</style>

```

* `index.js`
```python
import {createRouter, createWebHistory} from 'vue-router'
import AboutView from "@/views/AboutView.vue";
import LoginView from "@/views/LoginView.vue";
import RegisterView from "@/views/RegisterView.vue";
import MainView from "@/views/MainView.vue";
import WalletView from "@/views/WalletView.vue";
import ChartsView from "@/views/ChartsView.vue";



const router = createRouter({
    history: createWebHistory(import.meta.env.BASE_URL),
    routes: [
        {
            path: '/',
            name: 'about',
            component: AboutView
        },
        {
            path: '/login',
            name: 'login',
            component: LoginView
        },
        {
            path: '/register',
            name: 'register',
            component: RegisterView
        },
        {
            path: '/main',
            name: 'main',
            component: MainView
        },
        {
            path: '/personal',
            name: 'wallet',
            component: WalletView
        },
        {
            path: '/charts',
            name: 'chart',
            component: ChartsView
        },
    ]
})

export default router

```




