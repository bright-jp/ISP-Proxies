# Bright Data ISPプロキシ

[![Promo](https://github.com/luminati-io/ISP-Proxies/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://brightdata.jp/proxy-types/isp-proxies?promo=github15)

## Overview
ISPから直接取得したIPを使用して、安全で安定した高速なデータ収集を実現するために、Bright Dataの広範な[ISPプロキシネットワーク](https://brightdata.jp/proxy-types/isp-proxies)をご活用ください。

- **700,000+ ISP IP**
- 長期的に安定した**スタティックレジデンシャルIP**
- **99.9% 成功率**
- **HTTP(S) & SOCKS5 サポート**
- **国レベルのターゲティングが無料**

## Key Features
- **グローバルリーチ**: [複数の国](https://brightdata.jp/locations)にわたってISP IPへアクセスできます。
- **高い成功率**: Webサイトへのアクセスで最大99.9%の成功率です。
- **高速かつ安定**: 低レイテンシーと信頼性の高い稼働時間、99.99%のネットワーク可用性を提供します。
- **限定IPアクセス**: 一貫した接続のための専用IPです。
- **倫理的に取得**: すべてのISPプロキシはISPから直接取得され、GDPRおよびCCPAに準拠しています。

## Pricing Plans
- **従量課金（Pay As You Go）**: 月次コミットメントなしで$15/GB。
- **月額サブスクリプション - 共有（Shared）**:
  - **10 IPs**: $1.80/IP、$18/month + VAT。
  - **100 IPs**: $1.45/IP、$145/month + VAT。
  - **500 IPs**: $1.40/IP、$700/month + VAT。
  - **1,000 IPs**: $1.30/IP、$1300/month + VAT。
  - **Enterprise Plans**: 大規模なデータ収集ニーズ向けのカスタムソリューションです。
 
- **月額サブスクリプション - 専用（Dedicated）**:
  - **10 IPs**: $3.50/IP、$35/month + VAT。
  - **100 IPs**: $2.75/IP、$275/month + VAT。
  - **500 IPs**: $2.60/IP、$1300/month + VAT。
  - **1,000 IPs**: $2.50/IP、$2500/month + VAT。
  - **Enterprise Plans**: 大規模なデータ収集ニーズ向けのカスタムソリューションです。
 
- **月額サブスクリプション - Pay/GB**:
  - $12.75/GB、$499/month + VAT。
  - $11.25/GB、$999/month + VAT。
  - $10.50/GB、$1999/month + VAT。
  - **Enterprise Plans**: 大規模なデータ収集ニーズ向けのカスタムソリューションです。


登録すると、初回入金に対して1ドルごとに1ドルをマッチし、最大$500まで適用されます！

## Getting Started with ISP Proxies
1. **無料トライアルを開始**: クレジットカードは不要です。
2. **統合**: Bright DataのControl PanelまたはAPIを通じて、IPおよび設定を管理します。
3. **対応言語**: Python、Java、C#、Node.js、Shell向けのクイックスタートガイドが提供されています。

## Code Examples

### Python

```python
import sys

# Replace '[your customerID]', 'isp', and '[your password]' with your actual Bright Data customer ID, zone, and password
if sys.version_info[0] == 2:
    import six
    from six.moves.urllib import request
    opener = request.build_opener(
        request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())

if sys.version_info[0] == 3:
    import urllib.request
    opener = urllib.request.build_opener(
        urllib.request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())
```

### Java

```java
package example;

import org.apache.http.HttpHost;
import org.apache.http.client.fluent.*;

public class Example {
    public static void main(String[] args) throws Exception {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        HttpHost proxy = new HttpHost("brd.superproxy.io", 22225);
        String res = Executor.newInstance()
            .auth(proxy, "brd-customer-[your customerID]-zone-isp", "[your password]")
            .execute(Request.Get("https://geo.brdtest.com/mygeo.json").viaProxy(proxy))
            .returnContent().asString();
        System.out.println(res);
    }
}
```

### C#

```c#
using System;
using System.Net;

class Example
{
    static void Main()
    {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        var client = new WebClient();
        client.Proxy = new WebProxy("brd.superproxy.io:22225");
        client.Proxy.Credentials = new NetworkCredential("brd-customer-[your customerID]-zone-isp", "[your password]");
        Console.WriteLine(client.DownloadString("https://geo.brdtest.com/mygeo.json"));
    }
}
```

### Node.js

```node.js
require('request-promise')({
    url: 'https://geo.brdtest.com/mygeo.json',
    proxy: 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225',
})
.then(function(data){ console.log(data); },
    function(err){ console.error(err); });
```

### Shell

```shell
# Replace '[your customerID]' and '[your password]' with your actual credentials
curl --proxy brd.superproxy.io:22225 --proxy-user brd-customer-[your customerID]-zone-isp:[your password] -k "https://geo.brdtest.com/mygeo.json"
```

## Integrations
当社のISPプロキシは、以下を含む広く利用されている自動化ツールと互換性があります。

- [**Puppeteer**](https://brightdata.jp/integration/puppeteer)
- [**Selenium**](https://brightdata.jp/integration/selenium)
- [**Playwright**](https://brightdata.jp/integration/playwright)
- [**AdsPower**](https://brightdata.jp/integration/adspower)
- [**MultiLogin**](https://brightdata.jp/integration/multilogin)

## Use Cases
ISPプロキシの一般的な利用例:

- [**eCommerce**](https://brightdata.jp/use-cases/ecommerce): 価格および在庫状況を追跡します。
- [**Social Media**](https://brightdata.jp/use-cases/social-media-for-marketing): トレンドとエンゲージメントを監視します。
- [**Real Estate**](https://brightdata.jp/use-cases/real-estate): 物件掲載情報に関するデータを収集します。
- [**Travel**](https://brightdata.jp/use-cases/travel): 地域間で旅行取引を比較します。

## FAQ

### ISP Proxyとは何ですか？
ISPプロキシは、サーバーに割り当てられたスタティックレジデンシャルIPです。通常のレジデンシャルIPを使用しているかのようにコンテンツへアクセスできますが、より高い速度と安定性を提供します。

### ISP Proxiesはどのように動作しますか？
ISPプロキシはISPから直接提供されるIPを使用するため、レジデンシャルの視点を保ちながら、データセンター接続の速度でコンテンツへ高速かつ信頼性の高いアクセスを可能にします。

### ISP Proxiesを使用するメリットは何ですか？
ISPプロキシは、[レジデンシャルIP](https://brightdata.jp/proxy-types/residential-proxies)の安定性と匿名性に加え、データセンターIPの速度も提供します。Webスクレイピング、広告検証、SEOモニタリングなどのタスクに最適です。

### 企業はISP Proxiesをどのように使用していますか？
ISPプロキシは、制限されたコンテンツへのアクセス、広告の検証、競合サイトの監視、品質保証テストなどのタスクで広く利用されています。

### Bright DataのISP Proxiesは準拠していますか？
はい。すべてのISPプロキシは倫理的に取得され、GDPRおよびCCPAを含むデータ保護法に準拠しており、責任あるデータ運用を保証します。