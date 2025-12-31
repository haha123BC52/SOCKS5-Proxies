# Bright Data SOCKS5 プロキシ

[![Promo](https://github.com/bright-jp/SOCKS5-Proxies/blob/main/first-deposit-banner.PNG)](https://brightdata.jp/solutions/socks5-proxies) 

## Overview
Bright Data の Proxy Manager を使用して SOCKS5 プロキシサーバーへのリクエストを送信し、汎用性、匿名性、最高のパフォーマンスを実現するように設計された Bright Data の [SOCKS5 proxies](https://brightdata.jp/proxy-types/socks5-proxies) により、シームレスで高速なスクレイピングをお楽しみいただけます。

- **TCP および UDP トラフィックをサポート**
- **最大限の互換性を実現する SOCKS5 プロトコル**
- **99.99% の成功率**
- **無料のジオロケーションターゲティング（国、市、州、ZIP）**

## Key Features
- **グローバルカバレッジ**: [195 か国](https://brightdata.jp/locations)で利用可能な SOCKS5 プロキシ。
- **高い成功率**: スクレイピングおよびデータ収集で最大 99.99% の成功率。
- **高速レスポンス**: 遅延を最小限に抑えた信頼性の高い接続。
- **汎用的なプロトコル**: HTTP、HTTPS、FTP などに対応。
- **無制限のスケーリング**: 同時セッションに制限はありません。

## SOCKS5 Proxy Pricing

### Residential Proxies

- **Pay As You Go**: $8.4/GB、月額契約は不要です。
- **Monthly Subscriptions**:
  - **69 GB**: $7.14/GB、$499/月。
  - **158 GB**: $6.3/GB、$999/月。
  - **339 GB**: $5.88/GB、$1999/月。
  - **Enterprise Plans**: 大規模運用向けにカスタム価格とソリューションをご用意しています。

 ### ISP Proxies

- **Pay As You Go**: $1.8/IP、月額契約は不要です。
- **Monthly Subscriptions**:
  - **10 IPs**: $1.8/IP、$18/月。
  - **100 IPs**: $1.45/IP、$145/月。
  - **500 IPs**: $1.4/IP、$700/月。
  - **1,000 IPs**: $1.3/IP、$1,300/月。
  - **Enterprise Plans**: 1,000 IP を超える運用向けにカスタム価格とソリューションをご用意しています。
 
### Datacenter Proxies

- **Pay As You Go**: $1.40/IP、月額契約は不要です。
- **Monthly Subscriptions**:
  - **10 IPs**: $1.40/IP、$14/月。
  - **100 IPs**: $1.00/IP、$100/月。
  - **500 IPs**: $0.95/IP、$475/月。
  - **1,000 IPs**: $0.90/IP、$900/月。
  - **Enterprise Plans**: 1,000 IP を超える運用向けにカスタム価格とソリューションをご用意しています。

登録して、初回入金に対して最大 $500 まで 1 ドル単位で同額マッチを受け取れます！

## Getting Started with SOCKS5 Proxies
1. **無料トライアルを開始**: クレジットカードは不要です。
2. **統合**: Bright Data Proxy Manager または API を使用して SOCKS5 プロキシを管理します。
3. **対応プラットフォーム**: Python、Node.js、cURL などで SOCKS5 プロキシを簡単に設定できます。

## Code Examples

### Python

```python
import requests

proxy = {
    "http": "socks5h://[your username]:[your password]@brd.superproxy.io:22228",
    "https": "socks5h://[your username]:[your password]@brd.superproxy.io:22228"
}

response = requests.get("https://geo.brdtest.com/mygeo.json", proxies=proxy)
print(response.json())
```

### Node.js

```node.js
const request = require("request-promise");

const options = {
  url: "https://geo.brdtest.com/mygeo.json",
  proxy: "socks5h://[your username]:[your password]@brd.superproxy.io:22228",
};

request(options)
  .then(function (response) {
    console.log(response);
  })
  .catch(function (err) {
    console.error(err);
  });
```

### cURL

```shell
curl -x socks5h://brd.superproxy.io:22228 \
     --proxy-user [your username]:[your password] \
     "https://geo.brdtest.com/mygeo.json"
```

## Use Cases
さまざまな業界における SOCKS5 プロキシの汎用性をご覧ください。

- [**eCommerce**](https://brightdata.jp/use-cases/ecommerce): 複数地域の製品価格、レビュー、在庫状況を追跡します。
- [**Social Media**](https://brightdata.jp/use-cases/social-media-for-marketing): トレンド、エンゲージメント、競合の動向を匿名で監視します。
- [**Travel**](https://brightdata.jp/use-cases/travel): 正確なジオターゲティングにより、国や地域をまたいで旅行プランの料金を比較します。
- [**Financial Services**](https://brightdata.jp/use-cases/financial): リアルタイムの市場データを収集し、トレンドを安全に分析します。

---

## FAQ

### What is the SOCKS5 Proxy Protocol?
SOCKS5 は、プロキシを介してクライアントとサーバー間のネットワークパケットを中継する汎用的なプロキシプロトコルです。TCP と UDP の両方の接続をサポートしており、Webスクレイピング、制限の回避、匿名性の強化など、幅広い用途に利用できます。

### How does SOCKS5 differ from HTTP proxies?
SOCKS5 は HTTP プロキシよりも低いレベルで動作するため、HTTP、HTTPS、FTP、SMTP などを含む、より幅広い種類のトラフィックを処理できます。また、ネットワークパケットを変更しないため、より高い匿名性を提供します。

### How can I use SOCKS5 proxies with Bright Data services?
Bright Data は、Residential、Datacenter、ISP の各プロキシネットワークで SOCKS5 をサポートしています。SOCKS5 を使用するには、以下を実施します。
1. アプリケーションで、ポート `22228` の `brd.superproxy.io` を使用するように設定します。
2. 認証には Bright Data の認証情報を使用します。
3. `socks5h://` プロトコルでリモート DNS 解決を有効にします。

### What is the default port for SOCKS5 proxies?
Bright Data における SOCKS5 プロキシのデフォルトポートは `22228` です。HTTP（`22225`）および HTTPS（`22226`）の標準ポートは SOCKS5 接続には適用されない点にご注意ください。

### What are the benefits of using SOCKS5 proxies?
SOCKS5 プロキシには以下の利点があります。
- **高い匿名性**: IPアドレスをマスクし、安全でプライベートな接続を実現します。
- **汎用性**: HTTP、HTTPS、FTP など、複数種類のトラフィックを処理します。
- **制限の回避**: ジオブロック、ファイアウォール、検閲を回避します。
- **TCP と UDP のサポート**: 幅広いユースケースに適しています。
- **信頼できるパフォーマンス**: Bright Data の堅牢なインフラにより、高い稼働率と低遅延を実現します。

### How can I ensure the best performance with SOCKS5 proxies?
パフォーマンスを最適化するには、以下を実施してください。
1. ターゲットには IP ではなくドメイン名を使用します。
2. `socks5h://` プロトコルでリモート DNS 解決を設定します。
3. IP ローテーションやリクエスト最適化などの高度な機能には [Bright Data’s Proxy Manager](https://brightdata.jp/products/proxy-manager) を使用します。

### Can I perform geo-targeting with SOCKS5 proxies?
はい。Bright Data の SOCKS5 プロキシは、精密なジオターゲティングをサポートしています。username を変更することで、特定の国、市、州、ZIP コード、ASN をターゲットにできます（例: 米国の場合は `username-country-us`）。

### Are SOCKS5 proxies compliant with Bright Data's policies?
はい。Bright Data の SOCKS5 プロキシは GDPR および CCPA 規制に準拠しており、コンプライアンスと倫理的なデータ利用を保証します。コンプライアンスを維持するため、提供されるすべてのガイドラインに従ってください。

### What are the limitations of using SOCKS5 proxies?
- **IP の制限**: ドメイン名のみがサポートされ、直接の IP リクエストはブロックされます。
- **ポートの制限**: SOCKS5 接続ではポート `22228` を使用する必要があります。
- **リモート DNS 解決**: 準拠のために `socks5h://` プロトコルが必要です。
- **ターゲットポート**: `1024` を超えるポートのみをサポートします。