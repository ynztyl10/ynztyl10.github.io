---
layout:     post
title:      "简单好用的iTunes API"
subtitle:   "API介绍"
date:       2016-02-06 00:50:00
author:     "Lyang"
header-img: "img/post-bg-2016.jpg"
tags:
    - iTunes
    - AppStore
---



# 简单好用的iTunes API

最近需要抓取AppStore中应用的用户评论信息，做反馈聚合，找到几个比较有用的iTunes API，能够通过这些API来获取应用的信息（应用的基本信息、AppStore排行榜、应用的评价信息），而且这些API都是公开可用，并不需要爬虫什么的来抓取。


## iTunes Search APIs
最基本的搜索API，在苹果官网也有详细的[说明文档](http://www.apple.com/itunes/affiliates/resources/documentation/itunes-store-web-service-search-api.html)。

### lookup API
 根据app id获取app的详细信息，比如icon、售价、评论、截图等。

例如，书旗小说的app id是**733689509**

    https://itunes.apple.com/lookup?id=733689509

得到结果如下：

    {
    "resultCount": 1,
    "results": [
        {
            "artistViewUrl": "https://itunes.apple.com/us/developer/guang-zhou-li-ba-ba-wen-xue/id1025705471?uo=4",
            "artworkUrl60": "http://is5.mzstatic.com/image/thumb/Purple69/v4/36/71/72/36717229-e8ed-5078-b341-311e18413810/source/60x60bb.jpg",
            "artworkUrl100": "http://is5.mzstatic.com/image/thumb/Purple69/v4/36/71/72/36717229-e8ed-5078-b341-311e18413810/source/100x100bb.jpg",
            "screenshotUrls": [
                "http://a4.mzstatic.com/us/r30/Purple7/v4/81/c1/68/81c168f9-a9ec-5756-55e1-2645f7e6c57c/screen1136x1136.jpeg",
                "http://a4.mzstatic.com/us/r30/Purple5/v4/74/4e/5b/744e5b38-deb4-6974-cfd6-e4db0137aa5d/screen1136x1136.jpeg",
                "http://a4.mzstatic.com/us/r30/Purple7/v4/d2/ee/35/d2ee3599-e42c-b73a-7151-4bb2414a0125/screen1136x1136.jpeg",
                "http://a5.mzstatic.com/us/r30/Purple69/v4/a3/62/a6/a362a623-6528-66af-1292-dfb2b6f1e6b5/screen1136x1136.jpeg",
                "http://a5.mzstatic.com/us/r30/Purple7/v4/b7/d2/3e/b7d23efb-53f6-1e43-b695-e7015867ee25/screen1136x1136.jpeg"
            ],
            "ipadScreenshotUrls": [
                "http://a1.mzstatic.com/us/r30/Purple5/v4/4f/91/7d/4f917d66-63c6-dad8-8444-c1753336892d/screen480x480.jpeg",
                "http://a3.mzstatic.com/us/r30/Purple7/v4/7e/01/55/7e015576-7d80-bfd3-a782-7022c993240a/screen480x480.jpeg",
                "http://a3.mzstatic.com/us/r30/Purple5/v4/88/15/32/881532cb-1236-0398-92d2-59d22457941d/screen480x480.jpeg",
                "http://a4.mzstatic.com/us/r30/Purple7/v4/f8/ff/cf/f8ffcfc1-3153-1c06-d16f-eec10fe23607/screen480x480.jpeg",
                "http://a3.mzstatic.com/us/r30/Purple7/v4/a2/75/29/a27529b7-4aef-f59d-763e-490285785203/screen480x480.jpeg"
            ],
            "artworkUrl512": "http://is5.mzstatic.com/image/thumb/Purple69/v4/36/71/72/36717229-e8ed-5078-b341-311e18413810/source/512x512bb.jpg",
            "kind": "software",
            "features": [
                "iosUniversal"
            ],
            "supportedDevices": [
                "iPhone4",
                "iPad2Wifi",
                "iPad23G",
                "iPhone4S",
                "iPadThirdGen",
                "iPadThirdGen4G",
                "iPhone5",
                "iPodTouchFifthGen",
                "iPadFourthGen",
                "iPadFourthGen4G",
                "iPadMini",
                "iPadMini4G",
                "iPhone5c",
                "iPhone5s",
                "iPhone6",
                "iPhone6Plus",
                "iPodTouchSixthGen"
            ],
            "advisories": [
                "Infrequent/Mild Realistic Violence",
                "Infrequent/Mild Horror/Fear Themes",
                "Infrequent/Mild Cartoon or Fantasy Violence",
                "Infrequent/Mild Alcohol, Tobacco, or Drug Use or References",
                "Frequent/Intense Sexual Content or Nudity",
                "Frequent/Intense Mature/Suggestive Themes",
                "Infrequent/Mild Profanity or Crude Humor"
            ],
            "isGameCenterEnabled": false,
            "contentAdvisoryRating": "17+",
            "languageCodesISO2A": [
                "ZH"
            ],
            "trackViewUrl": "https://itunes.apple.com/us/app/shu-qi-xiao-shuo-shu-qi-zheng/id733689509?mt=8&uo=4",
            "trackCensoredName": "书旗小说 - 书旗正版最全的小说阅读器",
            "fileSizeBytes": "39761830",
            "trackContentRating": "17+",
            "currentVersionReleaseDate": "2016-02-04T10:05:31Z",
            "sellerName": "Guangzhou Alibaba Literature Information Technology Technology Co., Ltd.",
            "currency": "USD",
            "wrapperType": "software",
            "version": "2.4.2",
            "description": "必备小说阅读神器！必备电子书阅读神器！\n\n最全的小说！更新最快！新书最多！\n\n功能体验全面升级，大量小说！全网小说任你搜！\n\n更新及时，秒速提醒！新书推荐，懂你所想！\n\n增加出版物，心灵鸡汤成功励志口才演讲职场，等你来读！\n\n\n功能介绍：\n\n1、新增二十多万本热门书籍，让你看都看不完\n2、加强推荐，看完一本还有很多本\n3、加强搜索，搜书名搜作者搜标签\n4、还是搜索，还能智能纠正错别字\n5、优化细节体验，解决已知的bug\n\n我们的QQ用户群是“210651368”，热切盼望您的加入哈！后续有活动也会第一时间通知群里的书友们的，让我们一起把书旗做的更好！",
            "artistId": 1025705471,
            "artistName": "广州阿里巴巴文学信息技术有限公司",
            "genres": [
                "Books",
                "Entertainment"
            ],
            "price": 0,
            "releaseDate": "2014-01-30T21:54:29Z",
            "primaryGenreName": "Book",
            "primaryGenreId": 6018,
            "trackId": 733689509,
            "trackName": "书旗小说 - 书旗正版最全的小说阅读器",
            "bundleId": "com.shuqicenter.reader",
            "minimumOsVersion": "7.0",
            "genreIds": [
                "6018",
                "6016"
            ],
            "formattedPrice": "Free",
            "isVppDeviceBasedLicensingEnabled": true,
            "releaseNotes": "1、优化充值流程\n2、更快的检查更新，让你最快的看到大神更新\n3、开放大量限免书籍\n4、优化大量体验问题",
            "averageUserRating": 4.5,
            "userRatingCount": 12
        }
    ]
}

另外，还可以指定国家和区域，只需要在url中加上[国家和区域代码](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
例如，仅搜索中国地区：

    https://itunes.apple.com/cn/lookup?id=733689509

同时支持批量获取：

        https://itunes.apple.com/cn/lookup?id=733689509,733689510

### search API
就跟我们在AppStore应用中搜索应用一样，输入query，得到结果。
例如：

    https://itunes.apple.com/search?term=书旗小说&country=cn&media=software
    
同时还有很多参数可选：

    country：区分不同国家和区域的AppStore
    media：按类型过滤，比如software
    entity：返回按类型过滤，比如movie

其他参数和例子，可参考[官方API文档](http://www.apple.com/itunes/affiliates/resources/documentation/itunes-store-web-service-search-api.html)。

## iTunes RSS Feeds
RSS订阅，用于获取排行榜单，支持iPhone、iPad，任意分类下（游戏、效率等等）。

具体参数：

    genre：分类id
    limit：需要返回的topN

例如，获取**游戏**分类下，top10的iPad应用：

    https://itunes.apple.com/rss/toppaidapplications/limit=10/genre=6014/json

同样支持不同国家与区域：

    https://itunes.apple.com/cn/rss/toppaidapplications/limit=10/genre=6014/json
    
我们可以通过[ iTunes Store RSS Generator](https://rss.itunes.apple.com/cn/?urlDesc=)自行生成RSS订阅

## App Reviews
根据app id获取应用的评价信息API。
例如，获取书旗小说的用户评价：

    http://itunes.apple.com/rss/customerreviews/id=733689509/json

同样支持不同国家和区域：

    http://itunes.apple.com/cn/rss/customerreviews/id=733689509/json







