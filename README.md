# tvbox//又耳三登整合源
//代码主体为云星日记



{
  "lives": [{
    "group": "redirect",
    "channels": [{
      "name": "live",
      "urls": ["proxy://do=live&type=txt&ext=aHR0cDovLzUyYnNqLnZpcDo4MS9hcGkvdjMvZmlsZS9nZXQvMjk5MDIvMEVSY3pJMGJfekIudHh0P3NpZ249RHMyWW43SjY4eUVpN2FaS0pKcHUtN01hck1xZUlCLXlKbEotZGRacDJBVSUzRCUzQTA="]
    }]
  }],

  "wallpaper": "http://maoyingshi.cc/api.php",


  "spider": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/%E6%8E%A8%E8%8D%90%E5%8C%85jar/%E6%8E%A8%E8%8D%90%E5%8C%85.jar",
  //推荐包



  "spider": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/%E7%9B%B4%E6%92%ADjar/%E7%9B%B4%E6%92%AD.jar",
  //直播包






  // 首页推荐视频 (豆瓣)
  "recommend": [{
    "name": "豆瓣推荐",
    "request": {
      "method": "GET",
      "header": [{
        "key": "Referer",
        "value": "https://movie.douban.com/"
      }],
      "url": {
        "raw": "https://movie.douban.com/j/new_search_subjects?sort=U&range=0,10&tags=&playable=1&start=0&year_range=2022,2022"
      }
    },
    "response": {
      "result": "$.data",
      "data": [{
        "key": "name",
        "value": "title"
      },
        {
          "key": "note",
          "value": "rate"
        },
        {
          "key": "pic",
          "value": "cover"
        }]
    },
    "expires": "86400"
  }],


  // 首页推荐视频 (IMDb Popular Movies)
  "recommend": [{
    "name": "imdb",
    "request": {
      "method": "GET",
      "url": {
        "raw": "https://imdb-api.com/en/API/MostPopularMovies/k_1kz039kt"
      }
    },
    "response": {
      "result": "$.items",
      "data": [{
        "key": "name",
        "value": "title"
      },
        {
          "key": "note",
          "value": "imDbRating"
        },
        {
          "key": "pic",
          "value": "image"
        }]
    },
    "expires": "86400"
  }],


  // 评分 (数据来自 豆瓣)
  "rating": [{
    "name": "rating",
    "request": {
      "method": "GET",
      "url": {
        "raw": "https://api.wmdb.tv/api/v1/movie/search?q={name}&limit=1"
      }
    },
    "response": {
      "result": "this",
      "data": [{
        "key": "rating",
        "value": "doubanRating"
      }]
    }
  }],


  // 输入法智能联想接口
  //"association": [],

  // 中文分词接口
  "pullWord": [{
    "name": "pullWord",
    "request": {
      "method": "GET",
      "url": {
        "raw": "http://api.pullword.com/get.php?source={source}&param1=0&param2=0&json=1"
      }
    },
    "response": {
      "data": [{
        "key": "keyword",
        "value": "t"
      }]
    }
  }],

  // 字幕格式 (可选)
  "subtitle": {
    "color": "#FFFFFF",
    "size": "30"
  },




  "sites": [{
    "key": "djdjs",
    "name": "🙀DengC缝合源",
    "type": 3,
    "api": "",
    "searchable": 1,
    "quickSearch": 1,
    "filterable": 1
  },
    {
      "key": "3",
      "name": "🙀仅供自用",
      "type": 3,
      "api": "",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "douban",
      "name": "🔍豆瓣榜单1〔T4〕",
      "type": 4,
      "api": "http://t4.ganggang.live:3812/vod",
      "searchable": 0,
      "quickSearch": 0,
      "filterable": 0
    },
    {
      "key": "t4public",
      "name": "🔍豆瓣榜单2〔T4〕",
      "type": 4,
      "api": "https://t4.secan.icu/vod?sites=all&ali_token=阿里token&timeout=10",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 0
    },

    {
      "key":"Yyy",
      "name":"🦁在线直播〔SP〕",
      "api":"csp_YQKAPP",
      "type":3,
      "filterable":1,
      "playerType":2,
      "quickSearch":1,
      "searchable":1,
      "ext":"https://api-tx.shumaxc.xyz",
      "jar":"https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/XB%E5%8C%85jar/%E5%9C%A8%E7%BA%BF%E7%9B%B4%E6%92%AD.jar"
    },

    {
      "key": "jjnnj",
      "name": "🤖以下为官方资源🤖",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "4",
      "name": "🤖以下为官方资源🤖",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "SPQQ",
      "name": "🐧腾讯(官)",
      "type": 3,
      "api": "csp_QQ",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1,
      "jar": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/%E5%AE%98%E6%96%B9%E5%8C%85jar/%E5%AE%98%E6%96%B9.jar"
    },
    {
      "key": "SPIQY",
      "name": "🥝爱奇艺(官)",
      "type": 3,
      "api": "csp_IQIYI",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1,
      "jar": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/%E5%AE%98%E6%96%B9%E5%8C%85jar/%E5%AE%98%E6%96%B9.jar"
    },
    {
      "key": "MGT",
      "name": "🥭芒果(官)",
      "type": 3,
      "api": "csp_Mgtv",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1,
      "jar": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/%E5%AE%98%E6%96%B9%E5%8C%85jar/%E5%AE%98%E6%96%B9.jar"
    },
    {
      "key": "youku",
      "name": "👑优酷(官)",
      "type": 0,
      "api": "https://www.zycaiji.net:7788/api.php/provide/vod/from/youku/at/xml/",
      "searchable": 0,
      "quickSearch": 0,
      "filterable": 0,
      "categories": [
        "综艺",
        "动漫",
        "动作片",
        "喜剧片",
        "爱情片",
        "科幻片",
        "恐怖片",
        "剧情片",
        "战争片",
        "国产剧",
        "港台剧",
        "日韩剧",
        "欧美剧",
        "惊悚片",
        "犯罪片",
        "冒险片",
        "悬疑片",
        "动画片",
        "武侠片",
        "奇幻片",
        "少儿",
        "其他片"
      ],
      "jar": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/%E5%AE%98%E6%96%B9%E5%8C%85jar/%E5%AE%98%E6%96%B9.jar"
    },
    {
      "key": "csp_SP361",
      "name": "💘360(官)",
      "type": 3,
      "api": "csp_SP360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    //官方包
    {
      "key": "18",
      "name": "",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },

    {
      "key": "7",
      "name": "🤖以下为动漫资源🤖",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "kq",
      "name": "🤖以下为动漫资源🤖",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "csp_Anime1",
      "name": "🌸动漫大全",
      "type": 3,
      "api": "csp_Anime1",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1,
      "jar": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/%E6%8E%A8%E8%8D%90%E5%8C%85jar/%E6%8E%A8%E8%8D%90%E5%8C%85.jar"
    },
    {
      "key": "csp_Dm84",
      "name": "🚌动漫巴士",
      "type": 3,
      "api": "csp_Dm84",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "mtv_xp_异次动漫",
      "name": "🐯异次动漫　",
      "type": 3,
      "api": "csp_XPathMacFilter",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1,
      "ext": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/动漫包/异次元动漫.json"
    },
    {
      "key": "mtv_xp_动漫岛源",
      "name": "😸动漫岛源　",
      "type": 3,
      "api": "csp_XPathMacFilter",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1,
      "ext": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/动漫包/动漫岛.json"
    },
    {
      "key": "mtv_xp_去看动漫",
      "name": "🐮去看动漫　",
      "type": 3,
      "api": "csp_XBiubiu",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 0,
      "ext": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/动漫包/去看动漫.json"
    },


    {
      "key" : "drpy_js_AGE动漫",
      "name" : "🐸AGE动漫",
      "type" : 3,
      "api" : "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JAR/动漫包jar/age动漫.js",
      "ext" : "https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/动漫包/AGE动漫 (1).js"
    },
    {
      "key": "csp_biubiu_风车动漫",
      "name": "🍭风车动漫",
      "type": 3,
      "api": "csp_XBiubiu",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 0,
      "ext": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/动漫包/风车动漫.json"
    },
    {
      "key": "djsjsj",
      "name": "",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "8",
      "name": "🤖以下为直播资源🤖",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "djk",
      "name": "🤖以下为直播资源🤖",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "csp_XPath_鹅直播",
      "name": "⚽️体育直播",
      "type": 3,
      "api": "csp_XPath3",
      "searchable": 0,
      "quickSearch": 0,
      "filterable": 0,
      "ext": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/直播包/体育直播.json"
    },
    {
      "key": "csp_Yj1211",
      "name": "📱游戏直播",
      "type": 3,
      "api": "csp_Yj1211",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "py_huya",
      "name": "🐯虎牙",
      "type": 3,
      "api": "py_huya",
      "searchable": 0,
      "quickSearch": 0,
      "filterable": 1,
      "ext": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/直播包/虎牙.py"
    },
    {
      "key":"csp_XYQBiu_虎牙直播",
      "name":"🐯虎牙直播",
      "type":3,
      "api":"XYQBiu",
      "searchable":0,
      "quickSearch":0,
      "filterable":0,
      "ext":"https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/直播包/虎牙直播.json"
    },
    {
      "key": "py_douyu",
      "name": "🦈斗鱼",
      "type": 3,
      "api": "py_douyu",
      "searchable": 0,
      "quickSearch": 0,
      "filterable": 1,
      "ext": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/直播包/斗鱼.py"
    },
    {
      "key": "csp_biubiu_斗鱼",
      "name": "🦈斗鱼直播",
      "type": 3,
      "api": "csp_XYQBiu",
      "searchable": 0,
      "quickSearch": 0,
      "filterable": 0,
      "ext": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/直播包/斗鱼直播.json"
    },

    {
      "key": "csp_XYQ_lu1",
      "name": "️📺电视直播",
      "type": 3,
      "api": "csp_XYQHiker",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 0,
      "ext": "http://52bsj.vip:81/api/v3/file/get/61542/%E7%94%B5%E8%A7%86%E7%9B%B4%E6%92%AD%E6%BA%90.json?sign=JxgjHlxu8_IP1SK2AbvPOnG3dnOnOtvJE4V3TM0Vp1w%3D%3A0",
      "jar": "http://52bsj.vip:81/api/v3/file/get/61543/%E6%9C%80%E9%AB%981080%E5%93%94%E5%93%A9%E5%BF%B5%E5%BD%B1%E7%A5%9E%E9%A9%ACzb.jar?sign=BTFlwsHLsd9ID93zVjRQSvbbhRn8g4_KtO-cGrGthRI%3D%3A0"
    },


    {
      "key": "9",
      "name": "🤖以下为网盘资源🤖",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "y",
      "name": "🤖以下为网盘资源🤖",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key":"Upyunso",
      "name":"☁️up搜(仅搜索）",
      "type":3,
      "api":"csp_Upyunso",
      "playerType":1,
      "searchable":1,
      "quickSearch" :1,
      "filterable":0,
      "ext":"https://agit.ai/yimu/tv/raw/commit/3c1bed5fe1546705355e554267a162748696a789/token.txt",
      "jar":"https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/%E7%BD%91%E7%9B%98jar/up%E2%98%81%EF%B8%8F.jar"
    },
   
    {
      "key":"csp_Yisou",
      "name":"🔎易搜（仅支持搜索）",
      "type":3,
      "api":"csp_Yisou",
      "searchable":1,
      "quickSearch":1,
      "filterable":0,
      "ext":"https://agit.ai/yimu/tv/raw/commit/3c1bed5fe1546705355e554267a162748696a789/token.txt",
      "jar":"https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/%E7%BD%91%E7%9B%98jar/%E9%80%9A%E7%94%A8.jar"
    },
    {
      "key":"push_agent",
      "name":"🍭推送（爱优腾/磁力/阿里）",
      "type":3,
      "api":"csp_PushAgent",
      "searchable":0,
      "quickSearch":0,
      "filterable":0,
      "ext":"https://agit.ai/yimu/tv/raw/commit/3c1bed5fe1546705355e554267a162748696a789/token.txt",
      "jar":"https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/%E7%BD%91%E7%9B%98jar/%E9%80%9A%E7%94%A8.jar"
    },

    {
      "key": "10",
      "name": "🤖以下为娱乐资源🤖",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },

    {
      "key": "yule",
      "name": "🤖以下为娱乐资源🤖",
      "type": 3,
      "api": "360",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 1
    },
    {
      "key": "py_cctv",
      "name": "❤️爱央视",
      "type": 3,
      "api": "py_cctv",
      "searchable": 0,
      "quickSearch": 0,
      "filterable": 1,
      "ext": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/娱乐包/爱央视.py"
    },
    {
      "key":"csp_xBPQ_聚短视频",
      "name":"📽️聚短视频",
      "type":3,
      "api":"csp_xBPQ",
      "searchable":0,
      "quickSearch":0,
      "filterable":0,
      "ext":"https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/娱乐包/短视频.json",
      "jar": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/%E4%B8%80%E6%9C%A8%E6%BA%90/JAR/%E5%A8%B1%E4%B9%90jar/%E8%81%9A%E7%9F%AD%E8%A7%86%E9%A2%91.jar"
    },
    {
      "key": "csp_xpath_酷狗MV",
      "name": "🐶酷狗MV",
      "type": 3,
      "api": "csp_XYQBiu",
      "searchable": 0,
      "quickSearch": 0,
      "filterable": 0,
      "ext": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/娱乐包/酷狗mv.json"
    },
    {
      "key": "csp_xpath_kuqimv",
      "name": "🎤酷奇MV",
      "type": 3,
      "api": "csp_XYQBiu",
      "searchable": 0,
      "quickSearch": 0,
      "filterable": 0,
      "ext": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/娱乐包/酷奇mv.json"
    },
    {
      "key": "csp_biubiu_tingshuxb",
      "name": "🎧听书网",
      "type": 3,
      "api": "csp_XBiubiu",
      "searchable": 1,
      "quickSearch": 1,
      "filterable": 0,
      "ext": "https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JSON/娱乐包/听书网.json",
      "jar": "https://ghproxy.com/https://raw.githubusercontent.com/xianyuyimu/TVBOX-/main/一木源/JAR/娱乐jar/bili.jpg"
    }],

  "parses": [{
    "name": "解析聚合",
    "type": 3,
    "url": "Demo"
  },
    {
      "name": "Json并发",
      "type": 2,
      "url": "Parallel"
    },
    {
      "name": "Json轮询",
      "type": 2,
      "url": "Sequence"
    },
    {
      "name": "恩哥",
      "type": 1,
      "url": "http://newjiexi.gotka.top/keyu3.php?url=",
      "ext": {
        "flag": ["qq",
          "腾讯",
          "qiyi",
          "爱奇艺",
          "奇艺",
          "youku",
          "优酷",
          "mgtv",
          "芒果",
          "letv",
          "乐视",
          "pptv",
          "PPTV",
          "sohu",
          "bilibili",
          "哔哩哔哩",
          "哔哩"],
        "header": {
          "User-Agent": "okhttp/4.1.0"
        }
      }
    },
    {
      "name": "可遇不可求",
      "type": 1,
      "url": "http://newjiexi.gotka.top/keyu3.php?url=",
      "ext": {
        "flag": [
          "qq",
          "腾讯",
          "qiyi",
          "爱奇艺",
          "奇艺",
          "youku",
          "优酷",
          "mgtv",
          "芒果",
          "letv",
          "乐视",
          "pptv",
          "PPTV",
          "sohu",
          "bilibili",
          "哔哩哔哩",
          "哔哩"
        ],
        "header": {
          "User-Agent": "okhttp/4.1.0"
        }
      }
    },
    {
      "name": "bozrc",
      "type": 0,
      "url": "https://jx.bozrc.com:4433/player/?url=",
      "ext": {
        "flag": [
          "qq",
          "腾讯",
          "qiyi",
          "爱奇艺",
          "奇艺",
          "youku",
          "优酷",
          "mgtv",
          "芒果",
          "letv",
          "leshi",
          "LS",
          "pptv",
          "PPTV",
          "sohu",
          "bilibili",
          "哔哩哔哩",
          "哔哩"
        ],
        "header": {
          "User-Agent": ""
        }
      }
    },
    {
      "name": "rx2",
      "type": 1,
      "url": "http://rxjx.kuanjv.com/allm3u8.php?url="
    },
    {
      "name": "可与",
      "type": 1,
      "url": "http://newjiexi.gotka.top/keyu3.php?url=",
      "ext": {
        "flag": ["qq",
          "腾讯",
          "qiyi",
          "爱奇艺",
          "奇艺",
          "youku",
          "优酷",
          "mgtv",
          "芒果",
          "letv",
          "乐视",
          "pptv",
          "PPTV",
          "sohu",
          "bilibili",
          "哔哩哔哩",
          "哔哩"],
        "header": {
          "User-Agent": "okhttp/4.1.0"
        }
      }
    },
    {
      "name": "酷享影视",
      "type": 1,
      "url": "http://pandown.pro/app/kxjx.php?url=",
      "ext": {
        "flag": ["qq",
          "腾讯",
          "qiyi",
          "爱奇艺",
          "奇艺",
          "youku",
          "优酷",
          "mgtv",
          "芒果",
          "letv",
          "乐视",
          "pptv",
          "PPTV",
          "sohu",
          "bilibili",
          "哔哩哔哩",
          "哔哩"],
        "header": {
          "User-Agent": "okhttp/4.1.0"
        }
      }
    },

    {
      "name": "猫咪解析",
      "type": 0,
      "url": "https://jx.777jiexi.com/player/?url="
    },
    {
      "name": "parwix稳定",
      "type": 0,
      "ua": "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/39.0.2171.71 Safari/537.36",
      "url": "https://jx.bozrc.com:4433/player/?url="
    },



    {
      "name": "思古",
      "type": 0,
      "url": "https://jx.jsonplayer.com/player/?url="
    },
    {
      "name": "夜幕",
      "type": 0,
      "url": "https://www.yemu.xyz/?url="
    },
    {
      "name": "M3U8.TV",
      "type": 0,
      "url": "https://www.yemu.xyz/?url="
    },
    {
      "name": "RDHK",
      "type": 0,
      "url": "https://jx.rdhk.net/?v="
    },
    {
      "name": "虾米",
      "type": 0,
      "url": "https://jx.xmflv.com/?url="
    },
    {
      "name": "OK解析",
      "type": 0,
      "url": "https://okjx.cc/?url="
    },
    {
      "name": "腾讯",
      "type": 0,
      "url": "https://ckmov.ccyjjd.com/ckmov/?url="
    },
    {
      "name": "江湖①",
      "type": 1,
      "url": "http://211.99.99.236:4567/jhjson/ceshi.php?url="
    },

    {
      "name": "有点慢",
      "type": 0,
      "url": "https://jx.playerjy.com/?url="
    }],
  "ijk": [{
    "group": "软解码",
    "options": [{
      "category": 4,
      "name": "opensles",
      "value": "0"
    },
      {
        "category": 4,
        "name": "overlay-format",
        "value": "842225234"
      },
      {
        "category": 4,
        "name": "framedrop",
        "value": "1"
      },
      {
        "category": 4,
        "name": "soundtouch",
        "value": "1"
      },
      {
        "category": 4,
        "name": "start-on-prepared",
        "value": "1"
      },
      {
        "category": 1,
        "name": "http-detect-range-support",
        "value": "0"
      },
      {
        "category": 1,
        "name": "fflags",
        "value": "fastseek"
      },
      {
        "category": 2,
        "name": "skip_loop_filter",
        "value": "48"
      },
      {
        "category": 4,
        "name": "reconnect",
        "value": "1"
      },
      {
        "category": 4,
        "name": "enable-accurate-seek",
        "value": "0"
      },
      {
        "category": 4,
        "name": "mediacodec",
        "value": "0"
      },
      {
        "category": 4,
        "name": "mediacodec-auto-rotate",
        "value": "0"
      },
      {
        "category": 4,
        "name": "mediacodec-handle-resolution-change",
        "value": "0"
      },
      {
        "category": 4,
        "name": "mediacodec-hevc",
        "value": "0"
      },
      {
        "category": 1,
        "name": "dns_cache_timeout",
        "value": "600000000"
      }]
  },
    {
      "group": "硬解码",
      "options": [{
        "category": 4,
        "name": "opensles",
        "value": "0"
      },
        {
          "category": 4,
          "name": "overlay-format",
          "value": "842225234"
        },
        {
          "category": 4,
          "name": "framedrop",
          "value": "1"
        },
        {
          "category": 4,
          "name": "soundtouch",
          "value": "1"
        },
        {
          "category": 4,
          "name": "start-on-prepared",
          "value": "1"
        },
        {
          "category": 1,
          "name": "http-detect-range-support",
          "value": "0"
        },
        {
          "category": 1,
          "name": "fflags",
          "value": "fastseek"
        },
        {
          "category": 2,
          "name": "skip_loop_filter",
          "value": "48"
        },
        {
          "category": 4,
          "name": "reconnect",
          "value": "1"
        },
        {
          "category": 4,
          "name": "enable-accurate-seek",
          "value": "0"
        },
        {
          "category": 4,
          "name": "mediacodec",
          "value": "1"
        },
        {
          "category": 4,
          "name": "mediacodec-auto-rotate",
          "value": "1"
        },
        {
          "category": 4,
          "name": "mediacodec-handle-resolution-change",
          "value": "1"
        },
        {
          "category": 4,
          "name": "mediacodec-hevc",
          "value": "1"
        },
        {
          "category": 1,
          "name": "dns_cache_timeout",
          "value": "600000000"
        }]
    }],
  "ads": ["mimg.0c1q0l.cn",
    "www.googletagmanager.com",
    "www.google-analytics.com",
    "mc.usihnbcq.cn",
    "mg.g1mm3d.cn",
    "mscs.svaeuzh.cn",
    "cnzz.hhttm.top",
    "tp.vinuxhome.com",
    "cnzz.mmstat.com",
    "www.baihuillq.com",
    "s23.cnzz.com",
    "z3.cnzz.com",
    "c.cnzz.com",
    "stj.v1vo.top",
    "z12.cnzz.com",
    "img.mosflower.cn",
    "tips.gamevvip.com",
    "ehwe.yhdtns.com",
    "xdn.cqqc3.com",
    "www.jixunkyy.cn",
    "sp.chemacid.cn",
    "hm.baidu.com",
    "s9.cnzz.com",
    "z6.cnzz.com",
    "um.cavuc.com",
    "mav.mavuz.com",
    "wofwk.aoidf3.com",
    "z5.cnzz.com",
    "xc.hubeijieshikj.cn",
    "tj.tianwenhu.com",
    "xg.gars57.cn",
    "k.jinxiuzhilv.com",
    "cdn.bootcss.com",
    "ppl.xunzhuo123.com",
    "xomk.jiangjunmh.top",
    "img.xunzhuo123.com",
    "z1.cnzz.com",
    "s13.cnzz.com",
    "xg.huataisangao.cn",
    "z7.cnzz.com",
    "xg.huataisangao.cn",
    "z2.cnzz.com",
    "s96.cnzz.com",
    "q11.cnzz.com",
    "thy.dacedsfa.cn",
    "xg.whsbpw.cn",
    "s19.cnzz.com",
    "z8.cnzz.com",
    "s4.cnzz.com",
    "f5w.as12df.top",
    "ae01.alicdn.com",
    "www.92424.cn",
    "k.wudejia.com",
    "vivovip.mmszxc.top",
    "qiu.xixiqiu.com",
    "cdnjs.hnfenxun.com",
    "cms.qdwght.com"]
}
