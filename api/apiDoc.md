### 接口文档
+ 获取所有的小说列表
  ```
  + REST: get
  + addr: http://localhost:3000/api/xs_list
  + return:
    [{
        "headerImage": "http://res.cloudinary.com/idwzx/image/upload/v1472746056/dazhuzai_y6428k.jpg",
        "updateTime": "2017-02-17T14:59:59.744Z",
        "author": "天蚕土豆",
        "des": "大千世界，位面交汇，万族林立，群雄荟萃，一位位来自下位面的天之至尊，在这无尽世界，演绎着令人向往的传奇，追求着那主宰之路。 无尽火域，炎帝执掌，万火焚苍穹。 武境之内，武祖之威，震慑乾坤。 西天之殿，百战之皇，战威无可敌。 北荒之丘，万墓之地，不死之主镇天地。 ...... 少年自北灵境而出，骑九幽冥雀，闯向了那精彩绝伦的纷纭世界，主宰之路，谁主沉浮？ 大千世界，万道争锋，吾为大主宰。",
        "factionName": "大主宰",
        "sectionArray": [
          "58a70fef56d84738783c5fe8"
        ],
        "id": "58a70fef56d84738783c5fe9"
      },
      ........
    ]
  ```

+ 获取所有的小说内容
  ```
   + REST: get
   + addr: http://localhost:3000/api/xs_content
   + return:
      [
        {
          "sectionNum": 1,
          "sectionTitle": "测试章节",
          "sectionContent": "这是我存进去的第一章，仅供测试",
          "sectionResource": "百度贴吧",
          "recentUpdateTime": "2017-02-17T14:59:59.737Z",
          "id": "58a70fef56d84738783c5fe8"
        },
        ........
      ]
    ```

+ 登录
  ```
  + REST: post
  + addr: http://localhost:3000/api/Users/login
  + param: {"username":"lidikang", "password":"123456"},或者使用邮箱登录{"email":"andyliwr@outlook.com", "password":"123456"}
  + return:
      {
        "id": "iHVbNBiF3qZ7xJGozV8L4TiFr74OzRFgM5h4Ghf9AbHJkr0fZ3lQcCrLF5djIa5F",
        "ttl": 1209600,
        "created": "2017-02-18T05:46:48.473Z",
        "userId": "58a7bac76b2a300b88e22535"
      }
  ```

+ 注册
  ```
  + REST: post
  + addr: http://localhost:3000/api/Users
  + param: {
             "realm": "李迪康",
             "username": "lidikang",
             "password": "123456",
             "email": "andyliwr@outlook.com",
             "emailVerified": true,
            }
  + return:
      {
        "realm": "吴艳倩",
        "username": "wuyanqian",
        "email": "wuyanqian@myhexin.com",
        "emailVerified": false,
        "id": "58a7e0eff7cc7b0e84ad42fd"
      }
  ```

+ 获取排行榜
  ```
  + REST: get
  + addr: http://localhost:3000/api/xs_rank/getRank?rankType=zh
  + param: rankType=qd或者zh，分别代表获取起点排行榜，和纵横排行榜
  + return:
       "data": [
          {
            "standard": "汇总",
            "engName": "total",
            "zhRank": [
              {
                "num": 1,
                "factionName": "超品战兵",
                "author": "梁不凡",
                "headImg": "http://static.zongheng.com/upload/cover/10/1e/101ecef1545403f69722d665c41c7122.jpeg",
                "des": "萧兵原本是雇佣界的王者，却为了红颜知己而回归平凡都市，他一切从头开始，扮猪吃虎，逆流而上，脚底踩尸骨，怀搂美人腰，铸就王途霸业！    （微信公众号：梁不凡）",
                "url": "http://book.zongheng.com/book/512263.html"
              },
              .....
  ```
