# User Apidoc

## BasicInfo

### create_user Handler
- url:
http://localhost:20000/user/create_user
- method: `POST`
- params:
    - [ ] user_id: 用户 ID
    - [x] card_id: 一卡通 ID
    - [x] qq_id: QQ ID
    - [x] wechat_id: 微信 ID
    - [ ] stu_no: 学号
    - [ ] real_name: 真实姓名
    - [ ] nick_name: 昵称
    - [ ] gender: 性别
    - [ ] user_type: 用户类型
    - [ ] pwd: 密码
    - [ ] session: 用户 session
    - [x] mobile: 手机号

建议传的字段已勾选

- sample:

```py
data = {
    "qq_id":    123456,
    "card_id":  213141001,
    "wechat_id":123321,
    "mobile":   13900000000
}
requests.post("http://0.0.0.0:20000/user/create_user", data=data)
```

### get_user_by_uuid Handler
- url:
http://localhost:20000/user/get_user_by_uuid
- method: `GET`, `POST`
- params:
    - [x] uuid: 用户 UUID
- returns:
```json
{
    "code": 0,
    "data": {
        "card_id": 213141003,
        "wechat_id": 0,
        "stu_no": "",
        "real_name": "",
        "nick_name": "",
        "gender": 0,
        "user_type": 0,
        "identity": 1,
        "class": "",
        "dept_name": "",
        "major_name": "",
        "grade": 14,
        "qq_id": 111111111,
        "vip": 0,
        "vip_level": 0,
        "rmk_name": "",
        "hometown": "",
        "address": "",
        "birthday": ""
    },
    "message": ""
}
```