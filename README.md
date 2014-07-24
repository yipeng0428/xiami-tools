虾米工具包
============

* `Xiami.get_stared_song(self, uid=None)` 返回某用户所有收藏曲目列表, uid不写默认为登录用户. (测试速度过快会被ban, 一页等待1s)
* `Xiami.get_stared_collection(self, uid=None)` 返回某用户所有收藏精选集列表, uid不写默认为登录用户.
* `Xiami.get_stared_collection(self, uid=None)` 返回某用户所有收藏专集列表, uid不写默认为登录用户.
* `Xiami.set_320k()` 设置当前用户默认下载曲目为高音质
* `Xiami.download_song(self, song_id)` 返回编号为 *song_id* 的曲目的相关信息和下载地址, 详细返回请看范例
* `Xiami.download_album(self, album_id)` 返回编号为 *album_id* 的专辑的相关信息和专辑内曲目下载地址, 详细返回请看范例
* `Xiami.download_playlist(self, col_id)` 同上
* `Xiami.star_song(self, songid)` 收藏曲目编号为 *songid* 的歌曲

#### 范例

```python
xiami = Xiami('username', 'password')
print xiami.download_song(1773330029)

{'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330029_15326599_l.mp3?auth_key=xxx', 'header': {'Referer': 'http://img.xiami.com/static/swf/seiya/player.swf?v=1394535902294', 'User-Agent': 'Mozilla/5.0'}, 'cookies': {'member_auth': 'xxx', '_unsign_token': 'xxx', '__XIAMI_SESSID': 'xxx', 'user': 'xxx', '_xiamitoken': '88c977565b6f57d85833b488a43ac31c'}, 'data': [{'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'260', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Decision', 'album_id': u'204202267', 'id': 1773330029}]}
```

```python
xiami = Xiami('username', 'password')
print xiami.download_song(1773330029)

{'header': {'Referer': 'http://img.xiami.com/static/swf/seiya/player.swf?v=1394535902294', 'User-Agent': 'Mozilla/5.0'}, 'cookies': {'member_auth': '2W6bT45I621jiqifSIhiIC0f5O3VGGCFlo4Fj7Ev5VFwcdtaYYX%2FkauSRAJO2iKWrmFDReHNgWo', '_unsign_token': '1d753ca50994f5f5c07da420e4204430', '__XIAMI_SESSID': '047df5f493fdc1da653b74c48cdd8f08', 'user': '36962256%22lalala%22%222%22680%22%3Ca+href%3D%27%2Fwebsitehelp%23help9_3%27+%3Efa%3C%2Fa%3E%220%220%221597%223bba224459%221406222306', '_xiamitoken': '144df029292e13bec17db6feb9315be0'}, 'data': [{'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'260', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Decision', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330029_15326599_l.mp3?auth_key=25169b0959a1a19efe7ef44a74875867-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330029'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'126', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Best Thing That Ever Happened', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330030_15326600_l.mp3?auth_key=7607a2c3a8db52aa6442be2f35052c19-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330030'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'306', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'I&#039;m an Autobot', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330031_15326601_l.mp3?auth_key=19153a432b71ccfa55f02af6f7d3ee55-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330031'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'137', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Optimus Is Alive', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330032_15326602_l.mp3?auth_key=b510b3a5d023b31ec8182e5ca4c80746-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330032'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'353', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Cemetery Wind', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330033_15326603_l.mp3?auth_key=91411ca8bb8c972fd17ed9e323030d2c-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330033'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'317', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'His Name Is Shane and He Drives', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330034_15326604_l.mp3?auth_key=f46ee29ea1772555e48c27ad3298b35f-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330034'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'125', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Hacking the Drone', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330035_15326605_l.mp3?auth_key=885105789eab92cf93c8f91ee53236d0-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330035'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'204', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Transformium', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330036_15326606_l.mp3?auth_key=efb1be0087183fb01bcdade229e84a52-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330036'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'116', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Galvatron Is Online', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330037_15326607_l.mp3?auth_key=635937f4669a918b31051e01f1574324-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330037'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'206', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Your Creators Want You Back', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330038_15326608_l.mp3?auth_key=e131ed686ea5f3a8388f294879d34321-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330038'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'247', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'The Final Knight', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330039_15326609_l.mp3?auth_key=130bc1d5ab965c517c40e0617ab787d0-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330039'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'132', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Punch Hold Slide Repeat', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330040_15326610_l.mp3?auth_key=a32fc095a187b5c500cd926c7b8bf548-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330040'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'171', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'The Presence of Megatron', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330041_15326611_l.mp3?auth_key=0d1e881234f0e261900f5a882f9410c6-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330041'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'254', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Galvatron Is Active', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330042_15326612_l.mp3?auth_key=4efaeb48223726ed63556cefd52ddaa1-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330042'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'89', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Have Faith Prime', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330043_15326613_l.mp3?auth_key=ada5dcabfd8932ca8a9719933e7308cc-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330043'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'103', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Hong Kong Chase', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330044_15326614_l.mp3?auth_key=0aa27f22ad1dc4b03930b652c76bf974-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330044'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'76', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'The Legend Exists', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330045_15326615_l.mp3?auth_key=bc0e82e0ad64a4d6b906fef0a1b998d2-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330045'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'397', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Dinobot Charge', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330046_15326616_l.mp3?auth_key=4f0bdf9e12fef0ec036c1b85362b50e1-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330046'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'171', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'That&#039;s a Big Magnet', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330047_15326617_l.mp3?auth_key=9e3e0aec036311608b3a453cb321700f-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330047'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'125', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Drive Backwards', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330048_15326618_l.mp3?auth_key=e80004b10da22b2dab85d1d26cd63f96-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330048'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'318', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': u'http://img.xiami.net/lyric/49/1773330049_14053219446364.txt', 'title': u'Honor to the End', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330049_15326619_l.mp3?auth_key=9a32e62f902254ab97055a9d463a70dd-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330049'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'227', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Leave Planet Earth Alone', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330050_15326620_l.mp3?auth_key=07ce405bcc788d61d26798aece8e8163-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330050'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'201', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'The Knight Ship', 'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330051_15326621_l.mp3?auth_key=454f33bf388c817ce7e1a4ddbeb87268-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773330051'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'357', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': u'http://img.xiami.net/lyric/66/1773320966_14044862092251.lrc', 'title': u'Hunted', 'url': u'http://m5.file.xiami.com/566/58566/204202267/1773320966_15316504_l.mp3?auth_key=99a82d6c8dadd3f1b23df91908ee803e-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773320966'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'345', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': u'http://img.xiami.net/lyric/67/1773320967_14044862169970.lrc', 'title': u'Tessa', 'url': u'http://m5.file.xiami.com/566/58566/204202267/1773320967_15316505_l.mp3?auth_key=1353d214b36798b6240e9bf83df11b88-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773320967'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'177', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': u'http://img.xiami.net/lyric/68/1773320968_14044862276405.lrc', 'title': u'Autobots Reunite', 'url': u'http://m5.file.xiami.com/566/58566/204202267/1773320968_15316506_l.mp3?auth_key=84ecad921c74588ffe8ff34374f9974e-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773320968'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'294', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': u'http://img.xiami.net/lyric/69/1773320969_14044862358934.lrc', 'title': u'Lockdown', 'url': u'http://m5.file.xiami.com/566/58566/204202267/1773320969_15316507_l.mp3?auth_key=89334aa199686bda6ac580a04fac93da-1406332800-0-null', 'album_id': u'204202267', 'id': u'1773320969'}]}
```

一些其他好玩的组合
============
* 转移用户收藏数据
