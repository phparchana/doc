# BIGLYDROPSHIP API Documentation


# Contents
    1. Register
    2. Get Access Token
    3. Check through the access token 
    4. Get all the products in pagination . Per page 15 products
    5. Get Specific Product 
    6. To Delete the Product
    7. Update the Product
    8. Search the product through name and sku
    9. Add Product to Wishlist / Delete from WishList
    10. To Get all the orders
    11. To Order any product
    12. Add to cart API
    13. Delete product from Cart
    14. View All Cart Items of user
    15. Store Cart User Address
    16. Add Billing and Shiping Details  
    17. To View Users Billing and Shipping Address
    18. Update Shipping Address
    19. Delete Shipping Address
    20. Create order
    21. Contact Us
    22. My Orders
    23. Order Details
    24. Get Cancel Reasons
    25. Cancel Order
    26. My Profile
    27. Edit Profile
    28. Update Profile
    29. My WishLists
    30. Get Faqs
    31. Update Faqs
    32. Get all Notifications
    33. Check Profile Api
    34. View Bank Details of user
    35. Insert or Update Bank Details








##  Register through facebook (POST)

**API** `http://localhost:8000/api/login/fb`

**Method** : POST

### Request :

_Example_

```


{
    "access_token" : "EAAF6lwZAdOz8BAGf633RL6ZBEzBwJIaTm75mFQGZAyKM4uCN9BzVjnVrYtYLZB2J71YpJBjTqVN21xZBwddCHCAJgIfPq7qbePEE3CoW11K7k1oE6RIqLzoYYtKZAbzFCQx6291xqYzckQDWMSSAZAGO0mlUfsDgZCkP1SB8PqgQH1UeMSzIp9tPjoMbZBPZAQdHWP3sLsJEqLOK1zT3lP6wm2e7ysyZCYy6WsZD",
    "device_token" : "f5L9LXL2aOg:APA91bHfQaTRgzVjMWKUwQMdgNOiy96DA-C-4RXiFqT3DvWgsdPG6sIE_ZQccuJ04yz_9rFMZf4yAkX2lEX2n3FE7A0QPyTMbcwgwiGto4C5Qyj6GLBF3uuEJiEW86yWHl51YMMxLrkq",
    "device_type" : "ANDROID"
}

```


### Response :


_Example_

```
{
    "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6IjI3ODI5MDk4NDg4YzYxODIyZTM2ZTUzOGExMjBlMWI1OWJhNjVhMGIxMTBjODVlMmQ5OGNmNTY0NDUxNDJjNTJmNWNhZjkzMzk2OTA5MjIxIn0.eyJhdWQiOiIyNDYiLCJqdGkiOiIyNzgyOTA5ODQ4OGM2MTgyMmUzNmU1MzhhMTIwZTFiNTliYTY1YTBiMTEwYzg1ZTJkOThjZjU2NDQ1MTQyYzUyZjVjYWY5MzM5NjkwOTIyMSIsImlhdCI6MTUyODU0OTA0NiwibmJmIjoxNTI4NTQ5MDQ2LCJleHAiOjE1NjAwODUwNDYsInN1YiI6Ijk4OSIsInNjb3BlcyI6W119.Juftuv0kvw662XsR-8LEgx4ixlRmovy837YIg61i2vLHxumjb0JZ7lYNdMl_ktXHhzZBQB3wITDzDcBC8Awjv_MxkfcJ79UULX7FSRRBuKo5K0_pVFdjQmWPK9VSRA24TBc3upTnbzL_9Gj6lhxtrFma7DscBh_HGBFRYUskJl4H-3MJJ9JvCWFNjdjrHBiGNDXmSixzUlGZsO652PtpgY81TBXqOJ3yb1LrLZYyl5jDMXWWI3KfPKsCZSJWiyxowqNpYBYMa48-jCcqYPhbzaMORllWmgK5v2FLvLiJuQpXoZaUJ25k-MTljTuA0zt2cuAWot0a0PNIusDc6MoY8yBK16wRIA_mz5i4ZgkuPWdYtGC3oquSwwbTQ7gjeD0s2KMW5uGh-4P9HcDDMrNTdSgSj-CvwxNsfmXrbmQaEJCQieCr6gXHVfyo3oXVSjcnxhNbNUwj9-FEpLpPPfxfOw8Qj1woDNV-FRD89OQtH6sdbcXM0-akfyQT_sEJzjjHHZsd4_55pAk2nonLLFLJ8xxY0IPwPt0j0m5l3kDbBZvca2OEBPWUGs3GrIciDLltmTkcbg46_OHUrULBZ5spyK8IQZCGtwKb2f4HoG33PeU3yOZnYr0pJ2eDi8c3TMtQghGN_v-tjSj2zYo0nRF0hZvMxY16pA53S36iC3pbObg",
    "user": {
        "id": 989,
        "name": "Gunjan Kumar",
        "username": null,
        "email": "1618242761564460@facebook.com",
        "status": 1,
        "phone": "9039541384",
        "created_at": "May 24, 2018",
        "updated_at": "2018-06-09 18:26:50",
        "type": "client",
        "data": [
            {
                "user_id": 989,
                "name": "facebook.id",
                "value": "1618242761564460"
            },
            {
                "user_id": 989,
                "name": "tokens.fcm",
                "value": "f5L9LXL2aOg:APA91bHfQaTRgzVjMWKUwQMdgNOiy96DA-C-4RXiFqT3DvWgsdPG6sIE_ZQccuJ04yz_9rFMZf4yAkX2lEX2n3FE7A0QPyTMbcwgwiGto4C5Qyj6GLBF3uuEJiEW86yWHl51YMMxLrkq"
            },
            {
                "user_id": 989,
                "name": "tokens.fcm",
                "value": "f5L9LXL2aOg:APA91bHfQaTRgzVjMWKUwQMdgNOiy96DA-C-4RXiFqT3DvWgsdPG6sIE_ZQccuJ04yz_9rFMZf4yAkX2lEX2n3FE7A0QPyTMbcwgwiGto4C5Qyj6GLBF3uuEJiEW86yWHl51YMMxLrkq"
            },
            {
                "user_id": 989,
                "name": "tour",
                "value": "/dashboard,/orders,/products/import,/products/_,/products/_,/profile/company-information,/profile/bank-information,/orders/create,/products/_,/products,/products/_,/products/_,/products/_,/,/,/notification,/products/_,/products/_,/,/products/_"
            },
            {
                "user_id": 989,
                "name": "app_user",
                "value": "1"
            },
            {
                "user_id": 989,
                "name": "otp",
                "value": "4359"
            }
        ]
    },
    "mobile": 1
}

```
## Verify facebook mobile if mobile value is 0(POST)
**API** `http://localhost:8000/login/fb/mobile`

**Method** : POST

### Request :

_Example_

####Pass bearer access  token as header input(mandatory)

```
{
    "phone" : 9039541384
}
```
###Response : 

```
{
    "user": {
        "id": 989,
        "name": "Gunjan Kumar",
        "username": null,
        "email": "1618242761564460@facebook.com",
        "status": 1,
        "phone": "9039541384",
        "created_at": "May 24, 2018",
        "updated_at": "2018-06-09 18:26:50",
        "type": "client",
        "data": [
            {
                "user_id": 989,
                "name": "facebook.id",
                "value": "1618242761564460"
            },
            {
                "user_id": 989,
                "name": "tokens.fcm",
                "value": "f5L9LXL2aOg:APA91bHfQaTRgzVjMWKUwQMdgNOiy96DA-C-4RXiFqT3DvWgsdPG6sIE_ZQccuJ04yz_9rFMZf4yAkX2lEX2n3FE7A0QPyTMbcwgwiGto4C5Qyj6GLBF3uuEJiEW86yWHl51YMMxLrkq"
            },
            {
                "user_id": 989,
                "name": "tokens.fcm",
                "value": "f5L9LXL2aOg:APA91bHfQaTRgzVjMWKUwQMdgNOiy96DA-C-4RXiFqT3DvWgsdPG6sIE_ZQccuJ04yz_9rFMZf4yAkX2lEX2n3FE7A0QPyTMbcwgwiGto4C5Qyj6GLBF3uuEJiEW86yWHl51YMMxLrkq"
            },
            {
                "user_id": 989,
                "name": "tour",
                "value": "/dashboard,/orders,/products/import,/products/_,/products/_,/profile/company-information,/profile/bank-information,/orders/create,/products/_,/products,/products/_,/products/_,/products/_,/,/,/notification,/products/_,/products/_,/,/products/_"
            },
            {
                "user_id": 989,
                "name": "app_user",
                "value": "1"
            },
            {
                "user_id": 989,
                "name": "otp",
                "value": "4359"
            }
        ]
    },
    "otp": 2266
}
```

## Verify Otp (POST)

**API** `http://localhost:8000/api/verify`

**Method** : POST

### Request :

_Example_
```
{
    "otp" : 4359
}
```

###Response

```
{
    "status": "success"
}
```



## Register through Mobile Phone (Post)

**API** `http://localhost:8000/api/login/phone`

**Method** : POST

### Request :

_Example_
```
{
    "phone" : 9039541384
}
```

###Response

```
{
    "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6ImVhYjg1NDNhMzcwMTFjZTQzOTRhNzhkZjU2MmUxNGJjYTk3YTg4MDQ3ZThhZTgzMjcxMjA2MzgyZTAwNDg0ZGJiYWMxM2IzZGY0NmQxMGJmIn0.eyJhdWQiOiIyNDYiLCJqdGkiOiJlYWI4NTQzYTM3MDExY2U0Mzk0YTc4ZGY1NjJlMTRiY2E5N2E4ODA0N2U4YWU4MzI3MTIwNjM4MmUwMDQ4NGRiYmFjMTNiM2RmNDZkMTBiZiIsImlhdCI6MTUyODU1MTAyNywibmJmIjoxNTI4NTUxMDI3LCJleHAiOjE1NjAwODcwMjcsInN1YiI6IjEwMTgiLCJzY29wZXMiOltdfQ.aIN6qkNWnhNWv0Kf4aO-Wl_lwJpQD5EuaWYYnx4iAc5cAPquQvuOqIfUQz1GCgsJ4F1r2WkCtCWzpF7PYLdkVvhoHLxWmruwaFU-2AtbBPD7pHQU7vqyuClmiQhwPT9V-Eza60JNMdGLd0KEuItezXEq-sA9uLAA-0sJZHyHfM7aQ4iL_JpzZPn-NF_R_uZnqgYsEWtO84MWv5nCV-vYiqo0GYmtwr67AVkVi_xORKEyxsMyAQRVTCWbVFOx9mRT-a7K97EZ64d8tJvtx-ikaD3tLTddXW0qGWh9ggsh3dJc5zQeYbstQdpOyIOW5PCx_39NZ8EApUNDp_7uc1Nd85c_ugqpfubU8TVdujRbEMzrzrh6fjLa4bLttIip_k-QkqbBb5JFTsBlG_wVWU9tncV5AxSu3ERjdhlIJ5xphJ_-eAhmddTqxtBhS0A6Pg_I5FZd1ljyZiyk9WEZi27OQNVYFyVKo_W9aIEwPmxjT1zGZvaMgO2wYy4y0zhmQIznvtIDbQVv9O6ozeTn3s5SIQxREf-GZx-W0WrOj9XklVLESQ7kdO4tFVdYkJKwHcdaMrQWCA8i5XAuUEfgaL9pxzYVGD2_ciFqrYEDCl1lR89MzVW5Sm3H4wvskQrCt2RxwNDsJAQ8TJYdEDzKwOhABjqiciSRZodsBIcCRkCb34k",
    "user": {
        "name": "",
        "email": "9039541384@app.com",
        "type": "client",
        "updated_at": "2018-06-09 19:00:21",
        "created_at": "Jun 09, 2018",
        "id": 1018,
        "data": [
            {
                "user_id": 1018,
                "name": "app_user",
                "value": "1"
            },
            {
                "user_id": 1018,
                "name": "app_user",
                "value": "1"
            },
            {
                "user_id": 1018,
                "name": "tokens.fcm",
                "value": ""
            },
            {
                "user_id": 1018,
                "name": "app_user",
                "value": "1"
            },
            {
                "user_id": 1018,
                "name": "tokens.fcm",
                "value": ""
            },
            {
                "user_id": 1018,
                "name": "otp",
                "value": "4513"
            }
        ]
    },
    "otp": 5997
}
```


<!-- 2 -->

## Get Access Token (POST)

**API** `http://localhost:8000/oauth/token`

**Method** : POST

### Request :

_Example_

```

{
    "grant_type"        : "password",
    "client_id"         :  217,
    "username"          :  "sakshikbc@gmail.com",
    "client_secret"     : "FIK35PvZ4R8DKukpp9dPWNfTVzFUnA7mEAXGoTQh",
    "password"          : "123456"

}

```


### Response :


_Example_

```

{
    "token_type": "Bearer",
    "expires_in": 31536000,
    "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6ImNhNmM5Yjg1ODQxNTM1OTBhZGU2YjEwMDdhYjk2ZTlkNDA3ODM1ZTIwMDUyNjc3NGY4NWY3NGI5NGVjNWQ3MTlhZTY4MTEzMWIyZWI0ZTFjIn0.eyJhdWQiOiIyMTciLCJqdGkiOiJjYTZjOWI4NTg0MTUzNTkwYWRlNmIxMDA3YWI5NmU5ZDQwNzgzNWUyMDA1MjY3NzRmODVmNzRiOTRlYzVkNzE5YWU2ODExMzFiMmViNGUxYyIsImlhdCI6MTUyMzk0NDkxMCwibmJmIjoxNTIzOTQ0OTEwLCJleHAiOjE1NTU0ODA5MTAsInN1YiI6Ijc1OSIsInNjb3BlcyI6W119.TvpWVFQUtWxbgHvVoXhucGPOPv_pdfPX7Um_6pmeAHb3SQHpWPAven9lTfYcRZfwqMjE7BREpUfrlqGYynrmd9Kt-ty7VThlXvxi3HnHex9kN32jXmMxZhfECtx_Qnf3yqD2Enxy8dKkrxQYcKIru5-PA5DVPVLJ5RtvuiDzpMdM6gJf3Q1AT0cifK0GRYvojz7h-AoGdHAFrem_ceYic8kFWvv32JDIIU3mKmGHZGhZhTGK_hC_FsA-WyT7x848335O3onV_qZOuinduzRf9pY-aH61tby7USztzCwEWal_G8gQRaXnk1YTM9bcnklOBz5avbXH-902hqv8PUfBvwjIErOW1ybntO-VgheDEGeVT8d2y03W0U_U1_luoWmkwscL992l2yR_2FYvJ9T-sr19VMUsYJvVrYHcSlFmwfvFCM0dpomOSw1dBGvi0DJ0LeEYpCyAbrMVEtWA2Zgxq02JD8O3yQDv1enatLohweZ0VXtQWeNud32Chg1keRSAOuVHku53VE5JAOe-lx4NIHL3JYKVFkmLEsYMu-8SN7D2xPmG6FWLSAlHy7fafpTWwNlX3GFJz94zk12TMqp1rQVbor0VA74Ux6olxZecbxaCcDbxBZY60kOCeyHtPw9KI5WpSUdRuOajpxI1cJwp2uan_OMziippju-YBRlYrgc",
    "refresh_token": "def502009071e244a1cd030848c50c5b4ff83d166fb153a0c6f455697d11d204537a4210bc650afcdbd22d0235fb5405ade3e69c58713c0c17d4d159107b1c61be2b9a8e043c722447bde73cf72b82391ab2b6d79c34fade3f12c3649e900b8b5368893e0db6932e0e1a62787f21844772a51b81cc36f1327d0ef3a65e563f6b5fe8d7e9878ecb0116f8b3fbd7620267fd1af3305944d008cc5299cdad8a3c87f462dd65ebc889d4a2b3b738c1a947c42da0b40167c210ab91dd3a84f9d830423dc45656314fc3484ab7c33ee07383b93828697e3527305c4e59f59de2f26b071399c571b65c7695a84e5466ef8ffb9d6c9b982ba908758fc82bb0178ac4b49a7bc260ab47707d32751f587d5809a4fda7badf625c9cab1d47c65b4b24eae454e4185f3d97ad453924466ed6bf0fda6e151e3cde75abd721b35a33bbc458ac34ba271a3d162badd9ace4c43e0be45ef9664ca2a0c98acf5e8d4b007357e9d022af7cc4"
}


```

<!-- 3 -->

##  Get the access token 

**API** `http://localhost:8000/api/user`

**Method** : GET

### Header 

```
{
“Authorization” :  “Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6IjFkNTkzMTY3ODFkMzczMjY1MWRkNTVmMzNhMWJlNTczNjJhMDU1YWRjNjgyOTI0ODFkNGEwYzhkMDk2ZGYzMjczODJjZTdlMzQ3MDI1MTdhIn0.eyJhdWQiOiIxIiwianRpIjoiMWQ1OTMxNjc4MWQzNzMyNjUxZGQ1NWYzM2ExYmU1NzM2MmEwNTVhZGM2ODI5MjQ4MWQ0YTBjOGQwOTZkZjMyNzM4MmNlN2UzNDcwMjUxN2EiLCJpYXQiOjE1MjM1MDk4ODcsIm5iZiI6MTUyMzUwOTg4NywiZXhwIjoxNTU1MDQ1ODg3LCJzdWIiOiI1MTAiLCJzY29wZXMiOltdfQ.OgZCUJtxeq2RDEkElHGXIjWrA5o18_aD9ST9HFkZeAr_y8qmVtlSQiARN46FAtPqvYj0KIuj8q5Ca1QTB6Uc158TwB-H7CsgO_MadHSBTUdbwCOLCkbZlTvNRAEeq5KzFQGsYdI-FBfymg38k_MA7xlrvvW1QyjxyVEsFtpXNhr_Gv03c8kPIENYTBhTHWY7F4mnfSCPeLSaoKCbawp6SGS-tADaU25js2SY_m8AUsOuPw9-q-kTNEtHMIumYF_qpKBZXDaT7BbQ9XaX-k-BYgtAvm4nH_ApUPHNsLXMGQZzihgv0RSjUYN7TYQEgb411wjB3H1nZlRT9FGwn12lDV5QXxPTzHLAwqf_G9o6ZjkJh30X1SZS2zmSXjqGLWfB7TRcwsLpIn8NR97XJSvuArOey2hmif9BEs4j_weK6zHcc6Z99HhMlIwMQtBYV6tijm5z2CeYAbRTfn8EG8L8HZsuHdZzxUh_vqmRGooqJ80mcNGJ_cq5yJ0uXb7ZVGWbNAcxUBpoAjYYBTCZY20BZEaci8ocqvbp5B-S2o1jxPLyJ3HiGHtn-QSl8yKBYxgTH5ew_OtJZJk657gxfo4dBcxmhHcgbrHLM5hBGi4rqaD10V2CxLEMioyABtMoaCQyiFtMWj3r35J9OmofyZs-UMPE6p2dLv9EKlsYFlMtBMI”
}

```


### Response :


_Example_

```

{
    "id": 510,
    "name": "client",
    "username": null,
    "email": "client@seller.com",
    "status": 1,
    "phone": "1234567890",
    "created_at": "2018-03-03 07:23:29",
    "updated_at": "2018-03-03 07:23:29",
    "type": "client"
}


```


<!-- 4 -->


## Get all the products in pagination . Per page 15 products

**API** `http://localhost:8000/api/products`

`http://localhost:8000/api/products?q=query&category[]=51&vendor[]=514&vendor[]=2&price_range=501-1000`

**Method** : GET

### Response :


_Example_

```

{
    "products": {
        "current_page": 1,
        "data": [
            {
                "id": 24144,
                "user_id": 969,
                "name": "a sxhvn",
                "slug": "",
                "bdpin": "",
                "brand_id": 218,
                "model": "ffcgf",
                "sku": "cgf",
                "description": "87 7",
                "specification": "chbvhjvj ",
                "weight": "5785.00",
                "length": "87587.00",
                "width": "5.00",
                "height": "578.00",
                "amount": "8.00",
                "quantity": 6,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-06-07 14:17:56",
                "updated_at": "2018-06-07 14:18:35",
                "min_price": "9.00",
                "max_price": "10.00",
                "shipping_charge": "1.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "vgcg",
                "organization": {
                    "id": 933,
                    "user_id": 969,
                    "type_id": 0,
                    "name": "",
                    "logo": "",
                    "gst": "",
                    "incorporation_number": "",
                    "address": "",
                    "introduction": "",
                    "created_at": "2018-05-14 03:44:40",
                    "updated_at": "2018-05-14 03:44:40",
                    "city": "",
                    "state": "",
                    "pincode": "",
                    "country": ""
                },
                "categories": [
                    {
                        "id": 184,
                        "name": "sakshi",
                        "description": "svhavjss",
                        "meta_title": "dhiho",
                        "meta_des": "gujg",
                        "meta_keywords": "uj",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": []
            },
            {
                "id": 12583,
                "user_id": 254,
                "name": "General Knowledge 2019",
                "slug": "",
                "bdpin": "",
                "brand_id": 57,
                "model": "BDPIN10003",
                "sku": "BDPIN10003",
                "description": "\r\n\r\nGeneral Knowledge is the steady awareness towards progress of one’s surroundings. Building knowledge of all significant events and happenings requires consistency in learning on day to day basis and has also become essential for success in all competitions. General knowledge 2019 by Manohar Pandey comes as a comprehensive assimilation of factual information which proves useful for the aspirants of SSC, Bank, Railway, Police, NDA/CDS and Other Exams. With extensive coverage on current affairs, the book presents facts and figures with appropriate use of pictograms, graphics and tables for Simplified Learning and Easy Grasping. The syllabus for General Knowledge is broad and undefined and requires accurate, complete, topical coverage of facts from all walks of life.Covered in 5 chapters, one for each discipline, the book is a reliable and recommended source of information for anyone appearing in the forthcoming competitive exams.Table of ContentsCurrent AffairsHistory, Geography, Indian Polity, Indian Economy, General Science.\r\n\r\n",
                "specification": "\r\n\r\nPaperback:&nbsp;160 pagesPublisher:&nbsp;Arihant Publications; Eleventh edition (2018)Language:&nbsp;English\r\n\r\n",
                "weight": "100.00",
                "length": "20.00",
                "width": "0.60",
                "height": "13.00",
                "amount": "20.00",
                "quantity": 123,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-20 15:49:34",
                "updated_at": "2018-06-01 16:42:12",
                "min_price": "20.00",
                "max_price": "50.00",
                "shipping_charge": "30.00",
                "attributes": [],
                "isWishlist": true,
                "brand_name": "By Manohar Pandey",
                "organization": {
                    "id": 219,
                    "user_id": 254,
                    "type_id": 0,
                    "name": "Forbidden Retail",
                    "logo": "",
                    "gst": "Not provided yet",
                    "incorporation_number": "",
                    "address": "G-19 1st Floor Sector 3 Noida",
                    "introduction": "",
                    "created_at": "2018-02-20 15:21:07",
                    "updated_at": "2018-04-11 18:47:33",
                    "city": "Noida",
                    "state": "Uttar Pardesh",
                    "pincode": "201301",
                    "country": "India"
                },
                "categories": [
                    {
                        "id": 167,
                        "name": "Books",
                        "description": "a written or printed work consisting of pages glued or sewn together along one side and bound in covers.",
                        "meta_title": "Books",
                        "meta_des": "a written or printed work consisting of pages glued or sewn together along one side and bound in covers.",
                        "meta_keywords": "Books, Book",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": {
                    "id": 35910,
                    "user_id": 989,
                    "product_id": 12583,
                    "name": null,
                    "amount": null,
                    "created_at": null,
                    "updated_at": null,
                    "description": ""
                },
                "media": [
                    {
                        "id": 27558,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1519121995-41cme4z8c.jpg",
                        "small": "http://s.bigly.io/products/small/1519121995-41cme4z8c.jpg",
                        "medium": "http://s.bigly.io/products/medium/1519121995-41cme4z8c.jpg",
                        "large": "http://s.bigly.io/products/large/1519121995-41cme4z8c.jpg",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 12598,
                "user_id": 254,
                "name": "General Knowledge for All 2019",
                "slug": "",
                "bdpin": "",
                "brand_id": 67,
                "model": "BDPIN10012",
                "sku": "BDPIN10012",
                "description": "\r\n\r\nThe book ‘General Knowledge for All – 2019’ has been developed keeping in mind the requirements of school and college students and the aspirants of various competitive exams organised by UPSC, SSC, Banks, RBI, Railway, LIC, GIC, B.Ed, JBT/NTT, Army etc. and all other entrance and recruitment exams organised by various educational institutions and other establishments. As General Knowledge plays an important role in achieving success in almost every competitive examination, the main aim of the book is to present this vast subject in a concise, systematic and reader friendly manner to make the aspirants grasp its various topics easily and quickly. The book offers a rainbow of information on various subjects and topics in all major areas of study. There is subject wise general information on History, Geography, Polity, Defence, Economy, General Science, Sports, Awards and Honours and many other important subjects. The book will definitely prove to be a boon to all inquisitive students, exam aspirants and other readers in improving and enhancing their General Knowledge and will immensely help them perform better in their respective exams and competitions.Table of content: Our India; National Symbols; The Universe; United Nations Organisation; Defence; Transport; Indian Constitution and Polity; Planning in India; General Science; Space Research; Indian History; Important Dates of Indian History; World History; World Geography; First in India; Cultural Activities; Abbreviations; Awards; Sports.\r\n\r\n",
                "specification": "\r\n\r\nPublisher:&nbsp;Ramesh Publishing House (2018)Language:&nbsp;EnglishISBN-10:&nbsp;9387604187ISBN-13:&nbsp;978-9387604186\r\n\r\n",
                "weight": "100.00",
                "length": "21.30",
                "width": "2.20",
                "height": "13.80",
                "amount": "20.00",
                "quantity": 100,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-20 16:33:40",
                "updated_at": "2018-02-20 16:33:51",
                "min_price": "20.00",
                "max_price": "50.00",
                "shipping_charge": "30.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "By RPH Editorial Board",
                "organization": {
                    "id": 219,
                    "user_id": 254,
                    "type_id": 0,
                    "name": "Forbidden Retail",
                    "logo": "",
                    "gst": "Not provided yet",
                    "incorporation_number": "",
                    "address": "G-19 1st Floor Sector 3 Noida",
                    "introduction": "",
                    "created_at": "2018-02-20 15:21:07",
                    "updated_at": "2018-04-11 18:47:33",
                    "city": "Noida",
                    "state": "Uttar Pardesh",
                    "pincode": "201301",
                    "country": "India"
                },
                "categories": [
                    {
                        "id": 167,
                        "name": "Books",
                        "description": "a written or printed work consisting of pages glued or sewn together along one side and bound in covers.",
                        "meta_title": "Books",
                        "meta_des": "a written or printed work consisting of pages glued or sewn together along one side and bound in covers.",
                        "meta_keywords": "Books, Book",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 27581,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1519124694-51w9vdsnkp.jpg",
                        "small": "http://s.bigly.io/products/small/1519124694-51w9vdsnkp.jpg",
                        "medium": "http://s.bigly.io/products/medium/1519124694-51w9vdsnkp.jpg",
                        "large": "http://s.bigly.io/products/large/1519124694-51w9vdsnkp.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 12389,
                "user_id": 15,
                "name": "Wooddypeople COOL MEN'S BRACELET PURELY MADE OF GERMAN SILVER",
                "slug": "",
                "bdpin": "",
                "brand_id": 4,
                "model": "CVB-232",
                "sku": "CVB-232",
                "description": "You can wear this fashion jewellery on your outings wih friends or during performance or can gift it on birthdays or any special occassion. The design of this jewellery is such that it will make up your mood and add a glaomur to your attire.",
                "specification": "Latest Design",
                "weight": "20.00",
                "length": "9.00",
                "width": "1.00",
                "height": "9.00",
                "amount": "24.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-19 16:49:53",
                "updated_at": "2018-02-19 16:49:53",
                "min_price": "24.00",
                "max_price": "499.00",
                "shipping_charge": "50.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "Wooddypeople",
                "organization": {
                    "id": 58,
                    "user_id": 15,
                    "type_id": 1,
                    "name": "MAKO INTERNATIONAL PVT.LTD",
                    "logo": "",
                    "gst": "07AALCM1959L1ZW",
                    "incorporation_number": "",
                    "address": "FIRST FLOOR, H.NO.606, GALI KAIT WALI, SANGAT RASHAN BAZAR,, New Delhi, Delhi, 110055, NEW DELHI, DELHI, IN, 110055",
                    "introduction": "ECommerce",
                    "created_at": "2018-01-23 10:44:18",
                    "updated_at": "2018-02-13 15:41:30",
                    "city": "",
                    "state": "",
                    "pincode": "",
                    "country": ""
                },
                "categories": [
                    {
                        "id": 157,
                        "name": "Jewellery",
                        "description": "jjjjjj",
                        "meta_title": "jjjj",
                        "meta_des": "jjjj",
                        "meta_keywords": "jjjj",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 26993,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6MDNkNGRlODFmYWM3OTZkZWQzZmRmOWY2ZGViMDM3YWQ6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6MDNkNGRlODFmYWM3OTZkZWQzZmRmOWY2ZGViMDM3YWQ6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6MDNkNGRlODFmYWM3OTZkZWQzZmRmOWY2ZGViMDM3YWQ6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6MDNkNGRlODFmYWM3OTZkZWQzZmRmOWY2ZGViMDM3YWQ6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 26994,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NmU3MDJkY2JiYmRkMTQ5NzI2MTk3M2FkZjg3ODlmYjQ6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NmU3MDJkY2JiYmRkMTQ5NzI2MTk3M2FkZjg3ODlmYjQ6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NmU3MDJkY2JiYmRkMTQ5NzI2MTk3M2FkZjg3ODlmYjQ6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NmU3MDJkY2JiYmRkMTQ5NzI2MTk3M2FkZjg3ODlmYjQ6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 12250,
                "user_id": 15,
                "name": "Wooddypeople CLASSIC GERMAN SILVER BRACELET",
                "slug": "",
                "bdpin": "",
                "brand_id": 4,
                "model": "CVBR-012",
                "sku": "CVBR-012",
                "description": "You can wear this fashion jewellery on your outings wih friends or during performance or can gift it on birthdays or any special occassion. The design of this jewellery is such that it will make up your mood and add a glaomur to your attire.",
                "specification": "Latest Design",
                "weight": "20.00",
                "length": "9.00",
                "width": "1.00",
                "height": "9.00",
                "amount": "24.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-19 16:49:46",
                "updated_at": "2018-02-19 16:49:46",
                "min_price": "24.00",
                "max_price": "399.00",
                "shipping_charge": "50.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "Wooddypeople",
                "organization": {
                    "id": 58,
                    "user_id": 15,
                    "type_id": 1,
                    "name": "MAKO INTERNATIONAL PVT.LTD",
                    "logo": "",
                    "gst": "07AALCM1959L1ZW",
                    "incorporation_number": "",
                    "address": "FIRST FLOOR, H.NO.606, GALI KAIT WALI, SANGAT RASHAN BAZAR,, New Delhi, Delhi, 110055, NEW DELHI, DELHI, IN, 110055",
                    "introduction": "ECommerce",
                    "created_at": "2018-01-23 10:44:18",
                    "updated_at": "2018-02-13 15:41:30",
                    "city": "",
                    "state": "",
                    "pincode": "",
                    "country": ""
                },
                "categories": [
                    {
                        "id": 157,
                        "name": "Jewellery",
                        "description": "jjjjjj",
                        "meta_title": "jjjj",
                        "meta_des": "jjjj",
                        "meta_keywords": "jjjj",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 26756,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NTQ2ZWE4MGQ4YmYzNTBiOWUzMDlhZDFkZjJjMzgwODQ6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NTQ2ZWE4MGQ4YmYzNTBiOWUzMDlhZDFkZjJjMzgwODQ6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NTQ2ZWE4MGQ4YmYzNTBiOWUzMDlhZDFkZjJjMzgwODQ6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NTQ2ZWE4MGQ4YmYzNTBiOWUzMDlhZDFkZjJjMzgwODQ6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 26757,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZjU0YjczMmJmM2MzYTg0NTY3NDFkOTUzYzFmZWQ5ZWY6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZjU0YjczMmJmM2MzYTg0NTY3NDFkOTUzYzFmZWQ5ZWY6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZjU0YjczMmJmM2MzYTg0NTY3NDFkOTUzYzFmZWQ5ZWY6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZjU0YjczMmJmM2MzYTg0NTY3NDFkOTUzYzFmZWQ5ZWY6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 3685,
                "user_id": 131,
                "name": "Always Fit Anti Radiation Mobile Chip",
                "slug": "",
                "bdpin": "",
                "brand_id": 30,
                "model": "Nasa-034",
                "sku": "Nasa-034",
                "description": "Anti Radiation Sticker for Protection and better Health. An ISO 9001:2008 Certified company . Radiations can cause BRAIN TUMOR, HEART ATTACK, CANCER, RISK OF MISCARRIAGE. The Positive effects of ANTI RADIATION STICKER are: 1. Reduces radiation from electronic applied objects 2. Enhances sports performance 3. Help recover from sports fatigue 4. Increase in blood circulation 5. Helps to relax tensed muscles 6. Normalize physiological functions 7. Improves concentration and focus 8. Enhances body facility of oxygen 9. Strengthen the body's immune system 10. Reduces stress 11. Improves body energy 12. Relaxes migraine and headache 13. Lowers blood pressure 14. Enables a good night sleep 15. Relieves persistent neck and shoulders ache 16. Reduces back pain 17. Reduces sweat and odour take off the adhesive tape and paste the sticker on the product to reduce radiations",
                "specification": "Successfully reduce the harmful effects of EMF radiation by up to 90%. Can be used on SMARTPHONES, TABLETS, LAPTOPS, WIFI ROUTER.It acts as a barrier to protect brain and ear tissues from harmful radiation.\r\nAlso for design conscious people, CAN also be fixed inside the back cover of mobile phone. SO YOU CAN STILL USE YOUR FAVORITE MOBILE COVER WITHOUT HAMPERING ITS LOOK.\r\nAlso help in signal boosting of mobile phones & saves battery.",
                "weight": "5.00",
                "length": "4.00",
                "width": "2.00",
                "height": "1.00",
                "amount": "25.00",
                "quantity": 20,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-02 19:18:32",
                "updated_at": "2018-05-07 18:32:21",
                "min_price": "25.00",
                "max_price": "50.00",
                "shipping_charge": "35.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "Always Fit",
                "organization": {
                    "id": 97,
                    "user_id": 131,
                    "type_id": 0,
                    "name": "Nasa Care Life",
                    "logo": "",
                    "gst": "07AXJPN3435E1ZJ",
                    "incorporation_number": "",
                    "address": "2nd, Floor Dayal Market,, Narela Road, Alipur, NEW DELHI, DELHI, IN, 110036",
                    "introduction": "ECommerce",
                    "created_at": "2018-02-01 16:01:17",
                    "updated_at": "2018-03-08 16:52:55",
                    "city": "Satna",
                    "state": "Madhya Pradesh",
                    "pincode": "485001",
                    "country": "India"
                },
                "categories": [
                    {
                        "id": 6,
                        "name": "Health & Personal Care",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 11712,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1517579341-anti-radiation-mobile-chip-250x250.jpg",
                        "small": "media/small/1517579341-anti-radiation-mobile-chip-250x250.jpg",
                        "medium": "media/medium/1517579341-anti-radiation-mobile-chip-250x250.jpg",
                        "large": "http://localhost:8000/media/large/1517579341-anti-radiation-mobile-chip-250x250.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 12422,
                "user_id": 15,
                "name": " Wooddypeople STYLISH MEN'S CHAIN BY CRAFT VALLEY",
                "slug": "",
                "bdpin": "",
                "brand_id": 4,
                "model": "CVN-972",
                "sku": "CVN-972",
                "description": "You can wear this fashion jewellery on your outings wih friends or during performance or can gift it on birthdays or any special occassion. The design of this jewellery is such that it will make up your mood and add a glaomur to your attire.",
                "specification": "Latest Design",
                "weight": "20.00",
                "length": "20.00",
                "width": "20.00",
                "height": "1.00",
                "amount": "26.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-19 18:40:27",
                "updated_at": "2018-02-19 18:40:27",
                "min_price": "26.00",
                "max_price": "399.00",
                "shipping_charge": "50.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "Wooddypeople",
                "organization": {
                    "id": 58,
                    "user_id": 15,
                    "type_id": 1,
                    "name": "MAKO INTERNATIONAL PVT.LTD",
                    "logo": "",
                    "gst": "07AALCM1959L1ZW",
                    "incorporation_number": "",
                    "address": "FIRST FLOOR, H.NO.606, GALI KAIT WALI, SANGAT RASHAN BAZAR,, New Delhi, Delhi, 110055, NEW DELHI, DELHI, IN, 110055",
                    "introduction": "ECommerce",
                    "created_at": "2018-01-23 10:44:18",
                    "updated_at": "2018-02-13 15:41:30",
                    "city": "",
                    "state": "",
                    "pincode": "",
                    "country": ""
                },
                "categories": [
                    {
                        "id": 157,
                        "name": "Jewellery",
                        "description": "jjjjjj",
                        "meta_title": "jjjj",
                        "meta_des": "jjjj",
                        "meta_keywords": "jjjj",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 27146,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YTQ2OGRhZDlhZGQ1MzcwNjY4Yjg4Y2IxMTk3YjliMWU6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YTQ2OGRhZDlhZGQ1MzcwNjY4Yjg4Y2IxMTk3YjliMWU6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YTQ2OGRhZDlhZGQ1MzcwNjY4Yjg4Y2IxMTk3YjliMWU6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YTQ2OGRhZDlhZGQ1MzcwNjY4Yjg4Y2IxMTk3YjliMWU6Ojo6OjA=",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 27145,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ODVmODdjMDE4N2EwYWU1YzBiYTk5MTIxNWVlODFlN2I6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ODVmODdjMDE4N2EwYWU1YzBiYTk5MTIxNWVlODFlN2I6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ODVmODdjMDE4N2EwYWU1YzBiYTk5MTIxNWVlODFlN2I6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ODVmODdjMDE4N2EwYWU1YzBiYTk5MTIxNWVlODFlN2I6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 12380,
                "user_id": 15,
                "name": "Wooddypeople MEN'S BRACELET MADE OF GERMAN SILVER",
                "slug": "",
                "bdpin": "",
                "brand_id": 4,
                "model": "CVB-222",
                "sku": "CVB-222",
                "description": "You can wear this fashion jewellery on your outings wih friends or during performance or can gift it on birthdays or any special occassion. The design of this jewellery is such that it will make up your mood and add a glaomur to your attire.",
                "specification": "Latest Design",
                "weight": "20.00",
                "length": "9.00",
                "width": "1.00",
                "height": "9.00",
                "amount": "28.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-19 16:49:52",
                "updated_at": "2018-02-19 16:49:52",
                "min_price": "28.00",
                "max_price": "499.00",
                "shipping_charge": "50.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "Wooddypeople",
                "organization": {
                    "id": 58,
                    "user_id": 15,
                    "type_id": 1,
                    "name": "MAKO INTERNATIONAL PVT.LTD",
                    "logo": "",
                    "gst": "07AALCM1959L1ZW",
                    "incorporation_number": "",
                    "address": "FIRST FLOOR, H.NO.606, GALI KAIT WALI, SANGAT RASHAN BAZAR,, New Delhi, Delhi, 110055, NEW DELHI, DELHI, IN, 110055",
                    "introduction": "ECommerce",
                    "created_at": "2018-01-23 10:44:18",
                    "updated_at": "2018-02-13 15:41:30",
                    "city": "",
                    "state": "",
                    "pincode": "",
                    "country": ""
                },
                "categories": [
                    {
                        "id": 157,
                        "name": "Jewellery",
                        "description": "jjjjjj",
                        "meta_title": "jjjj",
                        "meta_des": "jjjj",
                        "meta_keywords": "jjjj",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 26974,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6N2I1MmJkZmEwMjVjM2E2NDM3ZjkwN2I0ZWJmMmYxOTQ6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6N2I1MmJkZmEwMjVjM2E2NDM3ZjkwN2I0ZWJmMmYxOTQ6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6N2I1MmJkZmEwMjVjM2E2NDM3ZjkwN2I0ZWJmMmYxOTQ6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6N2I1MmJkZmEwMjVjM2E2NDM3ZjkwN2I0ZWJmMmYxOTQ6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 26975,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6OWI1ZTY0NDE1NDcyZmQ2MDRhNWIxMDE0NDJlNDk3OTY6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6OWI1ZTY0NDE1NDcyZmQ2MDRhNWIxMDE0NDJlNDk3OTY6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6OWI1ZTY0NDE1NDcyZmQ2MDRhNWIxMDE0NDJlNDk3OTY6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6OWI1ZTY0NDE1NDcyZmQ2MDRhNWIxMDE0NDJlNDk3OTY6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 12241,
                "user_id": 15,
                "name": "Wooddypeople  BUY GERMAN SILVER BRACELET",
                "slug": "",
                "bdpin": "",
                "brand_id": 4,
                "model": "CVBR-003",
                "sku": "CVBR-003",
                "description": "You can wear this fashion jewellery on your outings wih friends or during performance or can gift it on birthdays or any special occassion. The design of this jewellery is such that it will make up your mood and add a glaomur to your attire.",
                "specification": "Latest Design",
                "weight": "7.00",
                "length": "9.00",
                "width": "1.00",
                "height": "9.00",
                "amount": "28.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-19 16:49:45",
                "updated_at": "2018-02-19 16:49:45",
                "min_price": "28.00",
                "max_price": "199.00",
                "shipping_charge": "50.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "Wooddypeople",
                "organization": {
                    "id": 58,
                    "user_id": 15,
                    "type_id": 1,
                    "name": "MAKO INTERNATIONAL PVT.LTD",
                    "logo": "",
                    "gst": "07AALCM1959L1ZW",
                    "incorporation_number": "",
                    "address": "FIRST FLOOR, H.NO.606, GALI KAIT WALI, SANGAT RASHAN BAZAR,, New Delhi, Delhi, 110055, NEW DELHI, DELHI, IN, 110055",
                    "introduction": "ECommerce",
                    "created_at": "2018-01-23 10:44:18",
                    "updated_at": "2018-02-13 15:41:30",
                    "city": "",
                    "state": "",
                    "pincode": "",
                    "country": ""
                },
                "categories": [
                    {
                        "id": 157,
                        "name": "Jewellery",
                        "description": "jjjjjj",
                        "meta_title": "jjjj",
                        "meta_des": "jjjj",
                        "meta_keywords": "jjjj",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 26738,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6MGEwMzczYzUyNDg1MzQxZTJlNWMzNzZmZWUzMGQyZTM6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6MGEwMzczYzUyNDg1MzQxZTJlNWMzNzZmZWUzMGQyZTM6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6MGEwMzczYzUyNDg1MzQxZTJlNWMzNzZmZWUzMGQyZTM6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6MGEwMzczYzUyNDg1MzQxZTJlNWMzNzZmZWUzMGQyZTM6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 26739,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NWZkZWVkZGNlN2I5YzAzMzYyMzg5NzQ5YmViZDZmYTI6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NWZkZWVkZGNlN2I5YzAzMzYyMzg5NzQ5YmViZDZmYTI6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NWZkZWVkZGNlN2I5YzAzMzYyMzg5NzQ5YmViZDZmYTI6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6NWZkZWVkZGNlN2I5YzAzMzYyMzg5NzQ5YmViZDZmYTI6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 12245,
                "user_id": 15,
                "name": "Wooddypeople ANTIQUE GERMAN SILVER BRACELET ONLINE",
                "slug": "",
                "bdpin": "",
                "brand_id": 4,
                "model": "CVBR-007",
                "sku": "CVBR-007",
                "description": "You can wear this fashion jewellery on your outings wih friends or during performance or can gift it on birthdays or any special occassion. The design of this jewellery is such that it will make up your mood and add a glaomur to your attire.",
                "specification": "Latest Design",
                "weight": "20.00",
                "length": "9.00",
                "width": "1.00",
                "height": "9.00",
                "amount": "28.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-19 16:49:45",
                "updated_at": "2018-02-19 16:49:45",
                "min_price": "28.00",
                "max_price": "199.00",
                "shipping_charge": "50.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "Wooddypeople",
                "organization": {
                    "id": 58,
                    "user_id": 15,
                    "type_id": 1,
                    "name": "MAKO INTERNATIONAL PVT.LTD",
                    "logo": "",
                    "gst": "07AALCM1959L1ZW",
                    "incorporation_number": "",
                    "address": "FIRST FLOOR, H.NO.606, GALI KAIT WALI, SANGAT RASHAN BAZAR,, New Delhi, Delhi, 110055, NEW DELHI, DELHI, IN, 110055",
                    "introduction": "ECommerce",
                    "created_at": "2018-01-23 10:44:18",
                    "updated_at": "2018-02-13 15:41:30",
                    "city": "",
                    "state": "",
                    "pincode": "",
                    "country": ""
                },
                "categories": [
                    {
                        "id": 157,
                        "name": "Jewellery",
                        "description": "jjjjjj",
                        "meta_title": "jjjj",
                        "meta_des": "jjjj",
                        "meta_keywords": "jjjj",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 26746,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YTA2YmQzZjU2NzllN2Y2OTVkMDE0MWU2NmZlYTE4MDc6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YTA2YmQzZjU2NzllN2Y2OTVkMDE0MWU2NmZlYTE4MDc6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YTA2YmQzZjU2NzllN2Y2OTVkMDE0MWU2NmZlYTE4MDc6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YTA2YmQzZjU2NzllN2Y2OTVkMDE0MWU2NmZlYTE4MDc6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 26747,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZmNlYTkxNGVkNmEzMmY0NGExMTYzZjBkMTQxNTYyZWU6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZmNlYTkxNGVkNmEzMmY0NGExMTYzZjBkMTQxNTYyZWU6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZmNlYTkxNGVkNmEzMmY0NGExMTYzZjBkMTQxNTYyZWU6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZmNlYTkxNGVkNmEzMmY0NGExMTYzZjBkMTQxNTYyZWU6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 12274,
                "user_id": 15,
                "name": "Wooddypeople STYLISH METALLIC GOLD PLATED UNISEX BRACELET BY CRAFTY 12",
                "slug": "",
                "bdpin": "",
                "brand_id": 4,
                "model": "CVBR-036",
                "sku": "CVBR-036",
                "description": "You can wear this fashion jewellery on your outings wih friends or during performance or can gift it on birthdays or any special occassion. The design of this jewellery is such that it will make up your mood and add a glaomur to your attire.",
                "specification": "Latest Design",
                "weight": "20.00",
                "length": "9.00",
                "width": "1.00",
                "height": "9.00",
                "amount": "28.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-19 16:49:47",
                "updated_at": "2018-02-19 16:49:47",
                "min_price": "28.00",
                "max_price": "499.00",
                "shipping_charge": "50.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "Wooddypeople",
                "organization": {
                    "id": 58,
                    "user_id": 15,
                    "type_id": 1,
                    "name": "MAKO INTERNATIONAL PVT.LTD",
                    "logo": "",
                    "gst": "07AALCM1959L1ZW",
                    "incorporation_number": "",
                    "address": "FIRST FLOOR, H.NO.606, GALI KAIT WALI, SANGAT RASHAN BAZAR,, New Delhi, Delhi, 110055, NEW DELHI, DELHI, IN, 110055",
                    "introduction": "ECommerce",
                    "created_at": "2018-01-23 10:44:18",
                    "updated_at": "2018-02-13 15:41:30",
                    "city": "",
                    "state": "",
                    "pincode": "",
                    "country": ""
                },
                "categories": [
                    {
                        "id": 157,
                        "name": "Jewellery",
                        "description": "jjjjjj",
                        "meta_title": "jjjj",
                        "meta_des": "jjjj",
                        "meta_keywords": "jjjj",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 26802,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YzI0NWZiMDI2ODkxZThjNzBlYTAzYTkxYzUxOWEyYWY6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YzI0NWZiMDI2ODkxZThjNzBlYTAzYTkxYzUxOWEyYWY6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YzI0NWZiMDI2ODkxZThjNzBlYTAzYTkxYzUxOWEyYWY6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6YzI0NWZiMDI2ODkxZThjNzBlYTAzYTkxYzUxOWEyYWY6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 26803,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZGY1MDExYTE2Zjk2M2I5OWYwMmM4MDMzYjk2YTFiZjQ6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZGY1MDExYTE2Zjk2M2I5OWYwMmM4MDMzYjk2YTFiZjQ6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZGY1MDExYTE2Zjk2M2I5OWYwMmM4MDMzYjk2YTFiZjQ6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZGY1MDExYTE2Zjk2M2I5OWYwMmM4MDMzYjk2YTFiZjQ6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 1490,
                "user_id": 72,
                "name": "micro to sd adapter",
                "slug": "",
                "bdpin": "",
                "brand_id": 21,
                "model": "MFT-SD Adaptor43",
                "sku": "MFT-SD Adaptor43",
                "description": "The Ultra microSDXC UHS-I Card lets you shoot and save more high-quality photos and Full HD (1) videos on your Android smartphone or tablet. From a world leader in flash memory storage, this card features a Class 10 speed rating for capturing Full HD video and read speeds of up to 80MB/s (2) for ultra-fast file transfer.",
                "specification": "products are constructed to the highest standards and rigorously tested. You can be confident in the outstanding quality, performance and reliability of every SanDisk produ",
                "weight": "50.00",
                "length": "1.50",
                "width": "1.00",
                "height": "1.00",
                "amount": "29.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-01-17 13:06:38",
                "updated_at": "2018-01-19 18:18:09",
                "min_price": "35.00",
                "max_price": "140.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "Maruti Febtech",
                "organization": {
                    "id": 39,
                    "user_id": 72,
                    "type_id": 0,
                    "name": "Maruti Febtech",
                    "logo": "media/company-logo/1jojl1fomk-1516087494.png",
                    "gst": "Not provided yet",
                    "incorporation_number": "",
                    "address": "283, new anand nagar near Rajendra Nagar A.B. road Indore 452012",
                    "introduction": "ECommerce",
                    "created_at": "2018-01-16 12:54:54",
                    "updated_at": "2018-03-22 16:44:02",
                    "city": "Indor",
                    "state": "Madhya Pradesh",
                    "pincode": "452012",
                    "country": "India"
                },
                "categories": [
                    {
                        "id": 33,
                        "name": "Mobile Accessories",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 7418,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1516184923-5468007028.jpeg",
                        "small": "media/small/1516184923-5468007028.jpeg",
                        "medium": "media/medium/1516184923-5468007028.jpeg",
                        "large": "http://localhost:8000/media/large/1516184923-5468007028.jpeg",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 7415,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1516184923-7380697727.jpeg",
                        "small": "media/small/1516184923-7380697727.jpeg",
                        "medium": "media/medium/1516184923-7380697727.jpeg",
                        "large": "http://localhost:8000/media/large/1516184923-7380697727.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 7416,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1516184923-8458112546.jpeg",
                        "small": "media/small/1516184923-8458112546.jpeg",
                        "medium": "media/medium/1516184923-8458112546.jpeg",
                        "large": "http://localhost:8000/media/large/1516184923-8458112546.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 7417,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1516184923-7484417119.jpeg",
                        "small": "media/small/1516184923-7484417119.jpeg",
                        "medium": "media/medium/1516184923-7484417119.jpeg",
                        "large": "http://localhost:8000/media/large/1516184923-7484417119.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 12421,
                "user_id": 15,
                "name": "Wooddypeople BEAUTIFUL MEN'S CHAIN MADE OF GERMAN SILVER BY CRAFT VALLEY",
                "slug": "",
                "bdpin": "",
                "brand_id": 4,
                "model": "CVN-971",
                "sku": "CVN-971",
                "description": "You can wear this fashion jewellery on your outings wih friends or during performance or can gift it on birthdays or any special occassion. The design of this jewellery is such that it will make up your mood and add a glaomur to your attire.",
                "specification": "Latest Design",
                "weight": "20.00",
                "length": "20.00",
                "width": "20.00",
                "height": "1.00",
                "amount": "35.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-19 18:40:27",
                "updated_at": "2018-04-24 17:41:14",
                "min_price": "35.00",
                "max_price": "55.00",
                "shipping_charge": "50.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "Wooddypeople",
                "organization": {
                    "id": 58,
                    "user_id": 15,
                    "type_id": 1,
                    "name": "MAKO INTERNATIONAL PVT.LTD",
                    "logo": "",
                    "gst": "07AALCM1959L1ZW",
                    "incorporation_number": "",
                    "address": "FIRST FLOOR, H.NO.606, GALI KAIT WALI, SANGAT RASHAN BAZAR,, New Delhi, Delhi, 110055, NEW DELHI, DELHI, IN, 110055",
                    "introduction": "ECommerce",
                    "created_at": "2018-01-23 10:44:18",
                    "updated_at": "2018-02-13 15:41:30",
                    "city": "",
                    "state": "",
                    "pincode": "",
                    "country": ""
                },
                "categories": [
                    {
                        "id": 157,
                        "name": "Jewellery",
                        "description": "jjjjjj",
                        "meta_title": "jjjj",
                        "meta_des": "jjjj",
                        "meta_keywords": "jjjj",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 27143,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZDFiMTdkODlkYzhjZTVmNTE1MTgxMWQ3NWEyZWI1NDk6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZDFiMTdkODlkYzhjZTVmNTE1MTgxMWQ3NWEyZWI1NDk6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZDFiMTdkODlkYzhjZTVmNTE1MTgxMWQ3NWEyZWI1NDk6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZDFiMTdkODlkYzhjZTVmNTE1MTgxMWQ3NWEyZWI1NDk6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 27144,
                        "mime": "",
                        "thumb": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZWM2YWFjNGQ2ZTg2ZTkyYzA3ZWZhZjA1MTM1YWMxNWY6Ojo6OjA=",
                        "small": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZWM2YWFjNGQ2ZTg2ZTkyYzA3ZWZhZjA1MTM1YWMxNWY6Ojo6OjA=",
                        "medium": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZWM2YWFjNGQ2ZTg2ZTkyYzA3ZWZhZjA1MTM1YWMxNWY6Ojo6OjA=",
                        "large": "https://nebula.wsimg.com/obj/ODEyRjM0RTk0OEEyMEMyNEZERDk6ZWM2YWFjNGQ2ZTg2ZTkyYzA3ZWZhZjA1MTM1YWMxNWY6Ojo6OjA=",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 12683,
                "user_id": 254,
                "name": "21 Anmol Kahaniyaa (Premchand)",
                "slug": "",
                "bdpin": "",
                "brand_id": 108,
                "model": "BDPIN10062",
                "sku": "BDPIN10062",
                "description": "With Premchand's versatile writing skill, the stories took a valuable space in indian literature. This book is an integration of 21 stories by Munshi Premchand, some of them are Ansuon ki holi, Namak ka Daroga, Shatranj ke Khiladi and many more.",
                "specification": "Reading level: 10+ yearsPaperback: 208 pagesPublisher: Maple Press; First edition (18 September 2015)Language: HindiISBN-10: 9350336618ISBN-13: 978-9350336618",
                "weight": "100.00",
                "length": "13.60",
                "width": "1.70",
                "height": "21.30",
                "amount": "35.00",
                "quantity": 99,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-21 00:15:58",
                "updated_at": "2018-04-05 15:03:24",
                "min_price": "35.00",
                "max_price": "100.00",
                "shipping_charge": "35.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "By PremChand",
                "organization": {
                    "id": 219,
                    "user_id": 254,
                    "type_id": 0,
                    "name": "Forbidden Retail",
                    "logo": "",
                    "gst": "Not provided yet",
                    "incorporation_number": "",
                    "address": "G-19 1st Floor Sector 3 Noida",
                    "introduction": "",
                    "created_at": "2018-02-20 15:21:07",
                    "updated_at": "2018-04-11 18:47:33",
                    "city": "Noida",
                    "state": "Uttar Pardesh",
                    "pincode": "201301",
                    "country": "India"
                },
                "categories": [
                    {
                        "id": 167,
                        "name": "Books",
                        "description": "a written or printed work consisting of pages glued or sewn together along one side and bound in covers.",
                        "meta_title": "Books",
                        "meta_des": "a written or printed work consisting of pages glued or sewn together along one side and bound in covers.",
                        "meta_keywords": "Books, Book",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 27714,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1519152380-51zvfgtgqx.jpg",
                        "small": "http://s.bigly.io/products/small/1519152380-51zvfgtgqx.jpg",
                        "medium": "http://s.bigly.io/products/medium/1519152380-51zvfgtgqx.jpg",
                        "large": "http://s.bigly.io/products/large/1519152380-51zvfgtgqx.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ]
            },
            {
                "id": 12593,
                "user_id": 254,
                "name": "One Indian Girl",
                "slug": "",
                "bdpin": "",
                "brand_id": 62,
                "model": "BDPIN10007",
                "sku": "BDPIN10007",
                "description": "\r\n\r\nHi, I'm Radhika Mehta and I'm getting married this week. I work at Goldman Sachs, an investment bank. Thank you for reading my story. However, let me warn you.You may not like me too much. One, I make a lot of money. Two, I have an opinion on everything. Three, I have had a boyfriend before. OK, maybe two.Now if all this was the case with a guy, one might be cool with it. But since I am a girl these three things I mentioned don’t really make me too likeable, do they?\r\n\r\n",
                "specification": "\r\n\r\nReading level:&nbsp;15.00+ yearsPaperback:&nbsp;280 pagesPublisher:&nbsp;Rupa Publications India; First edition (1 October 2016)Language:&nbsp;EnglishISBN-10:&nbsp;8129142147ISBN-13:&nbsp;978-8129142146\r\n\r\n",
                "weight": "100.00",
                "length": "13.20",
                "width": "1.60",
                "height": "19.80",
                "amount": "40.00",
                "quantity": 100,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-02-20 16:14:32",
                "updated_at": "2018-02-20 16:14:46",
                "min_price": "40.00",
                "max_price": "139.00",
                "shipping_charge": "40.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "By Chetan Bhagat",
                "organization": {
                    "id": 219,
                    "user_id": 254,
                    "type_id": 0,
                    "name": "Forbidden Retail",
                    "logo": "",
                    "gst": "Not provided yet",
                    "incorporation_number": "",
                    "address": "G-19 1st Floor Sector 3 Noida",
                    "introduction": "",
                    "created_at": "2018-02-20 15:21:07",
                    "updated_at": "2018-04-11 18:47:33",
                    "city": "Noida",
                    "state": "Uttar Pardesh",
                    "pincode": "201301",
                    "country": "India"
                },
                "categories": [
                    {
                        "id": 167,
                        "name": "Books",
                        "description": "a written or printed work consisting of pages glued or sewn together along one side and bound in covers.",
                        "meta_title": "Books",
                        "meta_des": "a written or printed work consisting of pages glued or sewn together along one side and bound in covers.",
                        "meta_keywords": "Books, Book",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null,
                "media": [
                    {
                        "id": 27576,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1519123497-51ka-upq61.jpg",
                        "small": "http://s.bigly.io/products/small/1519123497-51ka-upq61.jpg",
                        "medium": "http://s.bigly.io/products/medium/1519123497-51ka-upq61.jpg",
                        "large": "http://s.bigly.io/products/large/1519123497-51ka-upq61.jpg",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    }
                ]
            }
        ],
        "from": 1,
        "last_page": 623,
        "next_page_url": "http://localhost:8000/api/products?page=2",
        "path": "http://localhost:8000/api/products",
        "per_page": 15,
        "prev_page_url": null,
        "to": 15,
        "total": 9335
    },
    "filter": {
        "categories": [
            {
                "id": 179,
                "name": "Bike & Car-Accessories",
                "media": {
                    "id": 71002,
                    "mime": "",
                    "thumb": "http://s.bigly.io/categories/1528433579-bQBnwmEqPwjvUrw.jpeg",
                    "small": null,
                    "medium": null,
                    "large": null,
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                }
            },
            {
                "id": 167,
                "name": "Books",
                "media": null
            },
            {
                "id": 50,
                "name": "Camera & Photo",
                "media": null
            },
            {
                "id": 41,
                "name": "Computer Accessories",
                "media": null
            },
            {
                "id": 49,
                "name": "Electronic Accessories",
                "media": null
            },
            {
                "id": 58,
                "name": "Electronic appliances",
                "media": null
            },
            {
                "id": 6,
                "name": "Health & Personal Care",
                "media": {
                    "id": 71000,
                    "mime": "",
                    "thumb": "http://s.bigly.io/categories/1528374958-4GUUDlpmo3FKFIi.jpg",
                    "small": null,
                    "medium": null,
                    "large": null,
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                }
            },
            {
                "id": 19,
                "name": "Herbs & Seasonings",
                "media": {
                    "id": 71001,
                    "mime": "",
                    "thumb": "http://s.bigly.io/categories/1528375861-3CvrjzDmZUxfR8j.jpg",
                    "small": null,
                    "medium": null,
                    "large": null,
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                }
            },
            {
                "id": 43,
                "name": "Holi Colour",
                "media": null
            },
            {
                "id": 171,
                "name": "Home & Décor - Curtains",
                "media": null
            },
            {
                "id": 42,
                "name": "Home & Decor- Accessories",
                "media": null
            },
            {
                "id": 170,
                "name": "Home & Decor-Cushion Cover & Bedsheet",
                "media": null
            },
            {
                "id": 157,
                "name": "Jewellery",
                "media": null
            },
            {
                "id": 72,
                "name": "Jewelry Packaging & Display",
                "media": null
            },
            {
                "id": 44,
                "name": "Kitchen Masala",
                "media": null
            },
            {
                "id": 100,
                "name": "Luggage & Bags - Backpacks",
                "media": null
            },
            {
                "id": 103,
                "name": "Luggage & Bags - Handbags",
                "media": null
            },
            {
                "id": 104,
                "name": "Luggage & Bags - Luggage & Travel Bags",
                "media": null
            },
            {
                "id": 155,
                "name": "Luggage & Bags - Office Bags",
                "media": null
            },
            {
                "id": 156,
                "name": "Luggage & Bags - Sling Bags",
                "media": null
            },
            {
                "id": 105,
                "name": "Luggage & Bags - Special Purpose Bags",
                "media": null
            },
            {
                "id": 107,
                "name": "Luggage & Bags - Waist Packs",
                "media": null
            },
            {
                "id": 108,
                "name": "Luggage & Bags - Wallets & Holders",
                "media": null
            },
            {
                "id": 55,
                "name": "Men's Clothing",
                "media": null
            },
            {
                "id": 33,
                "name": "Mobile Accessories",
                "media": null
            },
            {
                "id": 151,
                "name": "Office and Stationary",
                "media": null
            },
            {
                "id": 172,
                "name": "Organic Products - Cleaners",
                "media": null
            },
            {
                "id": 173,
                "name": "Others",
                "media": null
            },
            {
                "id": 35,
                "name": "Pot Plant",
                "media": null
            },
            {
                "id": 184,
                "name": "sakshi",
                "media": null
            },
            {
                "id": 97,
                "name": "Shoes - Men's Shoes",
                "media": null
            },
            {
                "id": 60,
                "name": "Smart Electronics",
                "media": null
            },
            {
                "id": 150,
                "name": "Sunglasses",
                "media": null
            },
            {
                "id": 32,
                "name": "Watch",
                "media": null
            },
            {
                "id": 62,
                "name": "Women's Clothing",
                "media": null
            },
            {
                "id": 183,
                "name": "Womens Ethnic Wear",
                "media": null
            }
        ],
        "suppliers": [
            {
                "id": 1,
                "name": "TT Bags"
            },
            {
                "id": 15,
                "name": "MAKO INTERNATIONAL PVT.LTD"
            },
            {
                "id": 17,
                "name": "Importikah"
            },
            {
                "id": 19,
                "name": "Right Choice Bags"
            },
            {
                "id": 24,
                "name": "fatima purse"
            },
            {
                "id": 27,
                "name": "Aradhya retail corporation"
            },
            {
                "id": 28,
                "name": "Green Clean"
            },
            {
                "id": 31,
                "name": "Indiana Fabrics"
            },
            {
                "id": 32,
                "name": "Being Adam"
            },
            {
                "id": 37,
                "name": "SAHNI ENTERPRISES"
            },
            {
                "id": 72,
                "name": "Maruti Febtech"
            },
            {
                "id": 80,
                "name": "Lewis"
            },
            {
                "id": 86,
                "name": "SG Retails Hub Interior"
            },
            {
                "id": 94,
                "name": "TOTA"
            },
            {
                "id": 113,
                "name": "AKAY JEWELS"
            },
            {
                "id": 131,
                "name": "Nasa Care Life"
            },
            {
                "id": 132,
                "name": "ANAISHA ELECTRONICS"
            },
            {
                "id": 140,
                "name": "Akshay Worldwide Incorporation"
            },
            {
                "id": 145,
                "name": "Ankit Jain"
            },
            {
                "id": 146,
                "name": "sbc exports limited"
            },
            {
                "id": 170,
                "name": "Umesh Dhingra"
            },
            {
                "id": 197,
                "name": "Syed arshur rehmam"
            },
            {
                "id": 203,
                "name": "Navkar Creation"
            },
            {
                "id": 212,
                "name": "SVP Apparels Private Limited"
            },
            {
                "id": 240,
                "name": "Suman mihsra"
            },
            {
                "id": 243,
                "name": "Saurabh nim"
            },
            {
                "id": 245,
                "name": "Blueday Sales"
            },
            {
                "id": 254,
                "name": "Forbidden Retail"
            },
            {
                "id": 292,
                "name": "Aaditri Clothing"
            },
            {
                "id": 299,
                "name": "Dyas Fashions"
            },
            {
                "id": 323,
                "name": "Shibly"
            },
            {
                "id": 326,
                "name": "Anil Kumar visht"
            },
            {
                "id": 333,
                "name": "Rabia nishath"
            },
            {
                "id": 365,
                "name": "keshav sethia"
            },
            {
                "id": 409,
                "name": "As Traders"
            },
            {
                "id": 460,
                "name": "Exit9"
            },
            {
                "id": 481,
                "name": "Varsha"
            },
            {
                "id": 603,
                "name": "Shivani Agrawal"
            },
            {
                "id": 650,
                "name": "karan sonkar"
            },
            {
                "id": 707,
                "name": "MARCO"
            },
            {
                "id": 738,
                "name": "Gaurav rathor"
            },
            {
                "id": 826,
                "name": "Liya Fashion"
            },
            {
                "id": 828,
                "name": "Suhas"
            },
            {
                "id": 830,
                "name": "HIMANSHU GARG"
            },
            {
                "id": 845,
                "name": "ArbanChic"
            },
            {
                "id": 852,
                "name": "Gauri Agarwal"
            },
            {
                "id": 858,
                "name": "Bs shopping"
            },
            {
                "id": 876,
                "name": "JJ IMPEX"
            },
            {
                "id": 905,
                "name": "Deepak Jagwani"
            },
            {
                "id": 910,
                "name": "NIPUN MAHAJAN"
            },
            {
                "id": 947,
                "name": "Rajni Singh"
            },
            {
                "id": 957,
                "name": "Chinmey Rastogi"
            },
            {
                "id": 969,
                "name": "Rajkumar Jain"
            }
        ]
    },
    "responseCode": 200,
    "responseMessage": "Succesfull"
}
```

<!-- 5 -->

## Get Specific Product 

**API** `http://localhost:8000/api/products/1011`

**Method** : GET


### Response :


_Example_

```
{
    "product": {
        "id": 15,
        "user_id": 1,
        "name": "TT Bags Unisex Backpacks Blue Color With laptop Compartment",
        "slug": "",
        "bdpin": "",
        "brand_id": 1,
        "model": "BAG17s",
        "sku": "BAG17s",
        "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
        "specification": "Model Number\tBAG17s\r\nItem Height\t15 Centimeters\r\nItem Length\t20 Centimeters\r\nItem Width\t5 Centimeters\r\nVolume Capacity\t20 Liters\r\nItem Weight\t430 Grams\r\nMaterial\tPolyester\r\nSpecial Features\tZip Closure, Shoulder Strap, Laptop Compartment\r\nClosure\tZipper\r\nInner Material\tSatin\r\nStrap\tAdjustable\r\nWarranty Type\tManufacturer",
        "weight": "500.00",
        "length": "40.00",
        "width": "20.00",
        "height": "30.00",
        "amount": "399.00",
        "quantity": 20,
        "status": 1,
        "source": "bigly",
        "source_id": null,
        "created_at": "2017-11-18 19:20:27",
        "updated_at": "2018-05-08 23:02:20",
        "min_price": "399.00",
        "max_price": "1299.00",
        "shipping_charge": "75.00",
        "brand_name": "TT BAGS",
        "brand": {
            "id": 1,
            "name": "TT BAGS"
        },
        "organization": null,
        "categories": [
            {
                "id": 100,
                "name": "Luggage & Bags - Backpacks",
                "description": "",
                "meta_title": "",
                "meta_des": "",
                "meta_keywords": "",
                "slug": "",
                "parent_id": null,
                "status": 1
            }
        ],
        "attributes": [],
        "user": {
            "id": 1,
            "name": "TT Bags",
            "username": null,
            "email": "ttbags5@gmail.com",
            "status": 1,
            "phone": "9810795886",
            "created_at": "Nov 18, 2017",
            "updated_at": "2018-02-12 16:17:36",
            "type": "vendor"
        },
        "rating": null,
        "media": [
            {
                "id": 21,
                "mime": "image/jpeg",
                "thumb": "media/thumb/1511013060-17-1.jpg",
                "small": "media/small/1511013060-17-1.jpg",
                "medium": "media/medium/1511013060-17-1.jpg",
                "large": "http://localhost:8000/media/large/1511013060-17-1.jpg",
                "caption": null,
                "default": 0,
                "check": "pending"
            },
            {
                "id": 22,
                "mime": "image/jpeg",
                "thumb": "media/thumb/1511013061-17-2.jpg",
                "small": "media/small/1511013061-17-2.jpg",
                "medium": "media/medium/1511013061-17-2.jpg",
                "large": "http://localhost:8000/media/large/1511013061-17-2.jpg",
                "caption": null,
                "default": 0,
                "check": "pending"
            },
            {
                "id": 23,
                "mime": "image/jpeg",
                "thumb": "media/thumb/1511013062-17-3.jpg",
                "small": "media/small/1511013062-17-3.jpg",
                "medium": "media/medium/1511013062-17-3.jpg",
                "large": "http://localhost:8000/media/large/1511013062-17-3.jpg",
                "caption": null,
                "default": 0,
                "check": "pending"
            },
            {
                "id": 24,
                "mime": "image/jpeg",
                "thumb": "media/thumb/1511013063-17-4.jpg",
                "small": "media/small/1511013063-17-4.jpg",
                "medium": "media/medium/1511013063-17-4.jpg",
                "large": "http://localhost:8000/media/large/1511013063-17-4.jpg",
                "caption": null,
                "default": 0,
                "check": "pending"
            },
            {
                "id": 25,
                "mime": "image/jpeg",
                "thumb": "media/thumb/1511013064-17-5.jpg",
                "small": "media/small/1511013064-17-5.jpg",
                "medium": "media/medium/1511013064-17-5.jpg",
                "large": "http://localhost:8000/media/large/1511013064-17-5.jpg",
                "caption": null,
                "default": 0,
                "check": "pending"
            }
        ],
        "user_product": {
            "id": 35849,
            "user_id": 759,
            "product_id": 15,
            "name": "yo",
            "amount": "222.00",
            "created_at": null,
            "updated_at": null,
            "description": ""
        }
    },
    "isWishlist": false
}

```


<!-- 6 -->

## To Delete the product (DELETE)


**API** `http://localhost:8000/api/products/11`

**Method** : DELETE

### Request :

_Example_

```
{
    "user_id" : 510,
    "name": "Beeee-Watsica"
}

```


### Response :


_Example_

```

{
    1
}


```

<!-- 7 -->

## To update the product (PUT)


**API** `http://localhost:8000/api/products/1007`

**Method** : DELETE

### Request :

_Example_

```
{
    "user_id" : 510,
    "name": "cfdsgvd",
    "amount" : 54
}


```


### Response :


_Example_

```

{
    "user_id": 510,
    "product_id": "1007",
    "name": "cfdsgvd",
    "amount": 54,
    "updated_at": "2018-04-17 06:11:16",
    "created_at": "2018-04-17 06:11:16",
    "id": 1030
}



```


<!-- 8 -->

## Search the product through name and sku


**API** `localhost:8000/api/search?data=Keebler`
**API** `http://dropship.bigly.io/api/search?data=pro&&page=3`

**Method** : GET


### Response :


_Example_

```

{
    "current_page": 1,
    "data": [
        {
            "id": 16,
            "name": "Keebler and Sons",
            "slug": "",
            "bdpin": "ff65b07e-5662-3228-a30e-eae9416354e1",
            "brand_id": null,
            "model": null,
            "sku": "ae482e49-f59e-3c04-a24f-6e46b0867839",
            "description": "Lory positively sakshi to tell them something more. 'You promised to tell you--all I know is, it would be grand, certainly,' said Alice, and sighing. 'It IS a Caucus-race?' said Alice; 'you needn't.",
            "specification": null,
            "weight": "2210.00",
            "length": "6968.00",
            "width": "1199.00",
            "height": "2914.00",
            "amount": "51.00",
            "quantity": 0,
            "status": 1,
            "source": "bigly",
            "source_id": null,
            "created_at": "2018-03-01 10:54:50",
            "updated_at": "2018-03-01 10:54:50",
            "min_price": "0.00",
            "max_price": "0.00",
            "shipping_charge": "0.00",
            "brand_name": "",
            "brand": null,
            "categories": [
                {
                    "name": "Hyatt, Maggio and Russel"
                },
                {
                    "name": "Stracke PLC"
                },
                {
                    "name": "White, Boyer and Kuhlman"
                }
            ]
        },
        {
            "id": 29,
            "name": "Keebler-Baumbach",
            "slug": "",
            "bdpin": "d75a0b24-0b0e-3929-8334-32e94530208b",
            "brand_id": null,
            "model": null,
            "sku": "da295074-7ed2-3ec9-b8be-00960db66b85",
            "description": "Alice was not an encouraging opening for a good deal to come down the hall. After a minute or two, which gave the Pigeon in a court of justice before, but she gained courage as she ran; but the.",
            "specification": null,
            "weight": "652.00",
            "length": "7336.00",
            "width": "3303.00",
            "height": "9357.00",
            "amount": "53.00",
            "quantity": 0,
            "status": 1,
            "source": "bigly",
            "source_id": null,
            "created_at": "2018-03-01 10:54:51",
            "updated_at": "2018-03-01 10:54:51",
            "min_price": "0.00",
            "max_price": "0.00",
            "shipping_charge": "0.00",
            "brand_name": "",
            "brand": null,
            "categories": [
                {
                    "name": "Wunsch-Waters"
                }
            ]
        },
        {
            "id": 156,
            "name": "Brown, Keebler and Jacobi",
            "slug": "",
            "bdpin": "8841fe38-6bc3-3486-8518-15890d3ce33a",
            "brand_id": null,
            "model": null,
            "sku": "dbe74dc6-1446-38a3-a0d6-6b023a1c28ca",
            "description": "Duck and a Dodo, a Lory and an Eaglet, and several other curious creatures. Alice led the way, was the White Rabbit interrupted: 'UNimportant, your Majesty means, of course,' he said do. Alice.",
            "specification": null,
            "weight": "4360.00",
            "length": "9897.00",
            "width": "5539.00",
            "height": "9109.00",
            "amount": "29.00",
            "quantity": 0,
            "status": 1,
            "source": "bigly",
            "source_id": null,
            "created_at": "2018-03-01 10:54:56",
            "updated_at": "2018-03-01 10:54:56",
            "min_price": "0.00",
            "max_price": "0.00",
            "shipping_charge": "0.00",
            "brand_name": "",
            "brand": null,
            "categories": [
                {
                    "name": "Wiza-Doyle"
                }
            ]
        },
        {
            "id": 262,
            "name": "Keebler PLC",
            "slug": "",
            "bdpin": "6562faa3-7e48-3a3b-926a-999c4e07d3c5",
            "brand_id": null,
            "model": null,
            "sku": "90733f2d-65fe-3a0f-9df5-bbb4dbfcf05a",
            "description": "Alice, rather alarmed at the Queen, in a tone of delight, and rushed at the great puzzle!' And she tried the effect of lying down on the slate. 'Herald, read the accusation!' said the Gryphon, 'that.",
            "specification": null,
            "weight": "5193.00",
            "length": "4666.00",
            "width": "7041.00",
            "height": "3814.00",
            "amount": "43.00",
            "quantity": 0,
            "status": 1,
            "source": "bigly",
            "source_id": null,
            "created_at": "2018-03-01 10:55:00",
            "updated_at": "2018-03-01 10:55:00",
            "min_price": "0.00",
            "max_price": "0.00",
            "shipping_charge": "0.00",
            "brand_name": "",
            "brand": null,
            "categories": [
                {
                    "name": "Koepp and Sons"
                },
                {
                    "name": "Glover Group"
                },
                {
                    "name": "Tremblay-Pollich"
                }
            ]
        },
        {
            "id": 512,
            "name": "Keebler-Kutch",
            "slug": "",
            "bdpin": "4226a69b-4896-32c3-85c9-0770122a703a",
            "brand_id": null,
            "model": null,
            "sku": "de04fdce-645a-32df-871f-2ac43f2eb537",
            "description": "The Cat's head began fading away the time. Alice had no idea how to set about it; if I'm not used to come out among the bright eager eyes were nearly out of the Queen's voice in the other. In the.",
            "specification": null,
            "weight": "8073.00",
            "length": "2504.00",
            "width": "2850.00",
            "height": "9525.00",
            "amount": "24.00",
            "quantity": 0,
            "status": 1,
            "source": "bigly",
            "source_id": null,
            "created_at": "2018-03-01 10:55:10",
            "updated_at": "2018-03-01 10:55:10",
            "min_price": "0.00",
            "max_price": "0.00",
            "shipping_charge": "0.00",
            "brand_name": "",
            "brand": null,
            "categories": [
                {
                    "name": "Spencer Group"
                }
            ]
        },
        {
            "id": 579,
            "name": "Keebler-Pacocha",
            "slug": "",
            "bdpin": "5b17491d-992a-333d-8105-c8ebd7a133b9",
            "brand_id": null,
            "model": null,
            "sku": "06a7206c-0ca4-364c-849d-b736c1723d87",
            "description": "Mouse was speaking, so that by the officers of the crowd below, and there they lay sprawling about, reminding her very earnestly, 'Now, Dinah, tell me your history, she do.' 'I'll tell it her,' said.",
            "specification": null,
            "weight": "1696.00",
            "length": "8309.00",
            "width": "4582.00",
            "height": "4392.00",
            "amount": "34.00",
            "quantity": 0,
            "status": 1,
            "source": "bigly",
            "source_id": null,
            "created_at": "2018-03-01 10:55:12",
            "updated_at": "2018-03-01 10:55:12",
            "min_price": "0.00",
            "max_price": "0.00",
            "shipping_charge": "0.00",
            "brand_name": "",
            "brand": null,
            "categories": [
                {
                    "name": "Koepp and Sons"
                },
                {
                    "name": "Lynch, Jast and Osinski"
                },
                {
                    "name": "Wiza-Doyle"
                }
            ]
        }
    ],
    "from": 1,
    "last_page": 1,
    "next_page_url": null,
    "path": "http://localhost:8000/api/search",
    "per_page": 15,
    "prev_page_url": null,
    "to": 6,
    "total": 6
}
 




```



<!-- 9 -->

## Add WishList  or Delete ( POST ) 

**API** `http://localhost:8000/api/wishlist`

**Method** : POST

### Request :

_Example_

```
{
    "user_id" : 510,
    "product_id" : 1007
}


```


### Response :


_Example_

```

{
    "name": "Product",
    "wishlist": {
        "user_id": 510,
        "product_id": 1007,
        "updated_at": "2018-04-17 09:27:40",
        "created_at": "2018-04-17 09:27:40",
        "id": 10,
        "product": {
            "id": 1007,
            "name": "Product",
            "slug": "",
            "bdpin": "",
            "brand_id": 5,
            "model": "xgrfv",
            "sku": "szdgvxdhxd",
            "description": "<p>this is a great product</p>",
            "specification": "rtfgjhnc",
            "weight": "100.00",
            "length": "50.00",
            "width": "2.00",
            "height": "22525.00",
            "amount": "50.00",
            "quantity": 20,
            "status": 1,
            "source": "bigly",
            "source_id": null,
            "created_at": "2018-03-26 12:24:04",
            "updated_at": "2018-04-16 09:05:04",
            "min_price": "100.00",
            "max_price": "1000.00",
            "shipping_charge": "10.00",
            "brand_name": "fhdxcrhgcfgh",
            "brand": {
                "id": 5,
                "name": "fhdxcrhgcfgh"
            }
        }
    },
    "status": "Added to your wishlist"
}




```


<!-- 10 -->


## To get all the Orders


**API** `http://localhost:8000/api/orders`

**Method** : GET

### Response :

_Example_

```
{
    "current_page": 1,
    "data": [
        {
            "id": 98,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_BeaR3GHG1aW5eC3c",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-03 10:45:00",
            "updated_at": "2018-03-03 10:45:03",
            "status": "cancelled",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 99,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_zHqx6oauo1QuGnGu",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-03 10:47:16",
            "updated_at": "2018-03-03 10:47:16",
            "status": "placed",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 100,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_19QlPF9aDfbKuc2V",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-03 11:11:43",
            "updated_at": "2018-03-03 11:11:47",
            "status": "cancelled",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 101,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_YBsaWKJFx4iuNok0",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-03 11:12:14",
            "updated_at": "2018-03-03 11:12:14",
            "status": "placed",
            "price": "1500.00",
            "payment_method": "cod"
        },
        {
            "id": 102,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_KKg4ghvuMxSmZhY0",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-03 11:12:43",
            "updated_at": "2018-03-03 11:12:57",
            "status": "cancelled",
            "price": "1500.00",
            "payment_method": "cod"
        },
        {
            "id": 103,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_aKGbBHFLDxnAb4MZ",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-05 08:48:45",
            "updated_at": "2018-03-05 08:48:45",
            "status": "placed",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 104,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_34lC2g7nZw73tfQL",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-05 08:59:43",
            "updated_at": "2018-03-05 09:19:08",
            "status": "",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 105,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_GKLRvZogmdUdTjCM",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-05 09:27:12",
            "updated_at": "2018-03-05 09:27:12",
            "status": "placed",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 106,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_hTOFtWIke0eDkxlU",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-05 09:29:46",
            "updated_at": "2018-03-05 09:29:48",
            "status": "",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 107,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_1NFBrHEg8QoWoCqJ",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-05 09:30:14",
            "updated_at": "2018-03-05 09:31:45",
            "status": "",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 108,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_xUyrl00VgGSk2qSn",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-06 08:54:46",
            "updated_at": "2018-03-06 08:54:46",
            "status": "placed",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 109,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_OIZybPuLx490LAsJ",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-06 09:33:34",
            "updated_at": "2018-03-06 09:48:45",
            "status": "",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 110,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_IZumwmn1hS6qGcP0",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-06 09:40:26",
            "updated_at": "2018-03-06 09:40:26",
            "status": "placed",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 111,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_ZyUAOiJLdtPJkaui",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-06 09:51:32",
            "updated_at": "2018-03-06 09:51:35",
            "status": "",
            "price": "3000.00",
            "payment_method": "cod"
        },
        {
            "id": 112,
            "user_id": 510,
            "client_id": 510,
            "name": "DS_Order_ERglNzjPH0ijV6pf",
            "invoice": "",
            "amount": "300.00",
            "created_at": "2018-03-06 09:51:53",
            "updated_at": "2018-03-06 09:51:55",
            "status": "",
            "price": "3000.00",
            "payment_method": "cod"
        }
    ],
    "from": 1,
    "last_page": 4,
    "next_page_url": "http://localhost:8000/api/orders?page=2",
    "path": "http://localhost:8000/api/orders",
    "per_page": 15,
    "prev_page_url": null,
    "to": 15,
    "total": 50
}



```

<!-- 11 -->

## To Order any product (POST)


**API** `http://localhost:8000/api/orders`

**Method** : POST

### Request :

_Example_

```
{
      "first_name" : "sakshi",
      "last_name" : "kbc",
      "email" : "sakshi@gmail.com",
      "mobile" : "1234565789",
      "address_line_1" : "N 21 , Above United Bank of India",
      "address_line_2" : "N 21 , Above United Bank of India",
      "city" : "Satna",
      "state" : "Madhya Pradesh",
      "pincode" : "485001",
      "country" : "India",
      "payment_method" : "cod",
      "sameadd" : "Sameadd",
      "shipping_first_name" : "sakshi",
      "shipping_last_name" : "kbc",
      "shipping_address1" : "N 21 , Above United Bank of India",
      "shipping_address2" : "N 21 , Above United Bank of India",
      "shipping_city" : "Satna",
      "shipping_pincode" : "485001",
      "shipping_country" : "India",
      "shipping_state" : "Madhya Pradesh",
      "sku" : "szdgvxdhxd",
      "quantity" : "1",
      "shipping_charge" : "10.00",
      "products" : [
        {
                    "id" : 1007,
                    "name" : "Product",
                    "amount" : 50,
                    "quantity" : 10
        }
        
                ],
      "name": "Product",
      "amount" : 54
}



```


### Response :


_Example_

```

{
    "user_id": 510,
    "client_id": 1,
    "name": "Product",
    "price": 54,
    "amount": "50.00",
    "status": "placed",
    "payment_method": "cod",
    "updated_at": "2018-04-19 11:57:36",
    "created_at": "2018-04-19 11:57:36",
    "id": 167
}


```


<!-- 12 -->

## Add to cart API (POST)


**API** `http://localhost:8000/api/addToCart`

**Method** : POST

### Request :

_Example_

```
{
    "user_id" : 510,
    "product_id" : 1011,
    "quantity" : 10,
    "editedAmount" : 50,
    "paymentMode" : "COD",
    "size" : 50,
    "color" : "blue",
    "type" : "cart"
}

```


### Response :


_Example_

```
{
    "cart": {
        "id": 52,
        "user_id": 759,
        "product_id": 1011,
        "attribute_id": 0,
        "quantity": 10,
        "amount": 50,
        "payment_mode": "COD",
        "status": 1,
        "type": "cart",
        "created_at": "2018-05-22 15:43:22",
        "updated_at": "2018-05-22 15:43:22",
        "product": {
            "id": 1011,
            "user_id": 19,
            "name": "Right Choice,women's-Girls-Ladies-Laptop Sholder Handbags Online in India Black (RCH15 103)",
            "slug": "",
            "bdpin": "",
            "brand_id": 12,
            "model": "RCH15 103",
            "sku": "RCH15 103",
            "description": "Right Choice Girls-Ladies-Laptop Sholder Handbags Material : P.U - Colour :Black - Type : Casual Dimensions L X H X W (cm) : 47 x 29 x 12 (cm) Strap Type &amp; Closure Type : Belt-Zip Capacity &amp; Pockets : 2 kg-6+1 mobile pocket Warranty : 12 month On Manufacturing Defect With Replacement.",
            "specification": "\r\n\r\nWomen handbag laptop slot with velcro fastener\r\n\r\n",
            "weight": "450.00",
            "length": "47.00",
            "width": "29.00",
            "height": "12.00",
            "amount": "456.00",
            "quantity": 10,
            "status": 1,
            "source": "bigly",
            "source_id": null,
            "created_at": "2017-12-28 14:46:27",
            "updated_at": "2018-02-23 11:17:46",
            "min_price": "456.00",
            "max_price": "1299.00",
            "shipping_charge": "75.00",
            "brand_name": "Right Choice Bags",
            "brand": {
                "id": 12,
                "name": "Right Choice Bags"
            },
            "organization": {
                "id": 13,
                "user_id": 19,
                "type_id": 0,
                "name": "Right Choice Bags",
                "logo": "http://s.bigly.io/logo/1523474088-yTmwG6zmSXM6yAA.jpg",
                "gst": "36AJPPA8431P1ZO",
                "incorporation_number": "",
                "address": "12-1-487/b/11/51/9 huda colony\r\nasifnagar\r\nhyderabad TELANGANA\r\nIndia 500028",
                "introduction": "ECommerce",
                "created_at": "2017-12-28 14:25:05",
                "updated_at": "2018-04-12 00:44:48",
                "city": "hyderabad",
                "state": "TELANGANA",
                "pincode": "500028",
                "country": "India"
            },
            "media": [
                {
                    "id": 4883,
                    "mime": "image/jpeg",
                    "thumb": "media/thumb/1514625166-1.jpg",
                    "small": "media/small/1514625166-1.jpg",
                    "medium": "media/medium/1514625166-1.jpg",
                    "large": "http://localhost:8000/media/large/1514625166-1.jpg",
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                },
                {
                    "id": 4884,
                    "mime": "image/jpeg",
                    "thumb": "media/thumb/1514625172-2.jpg",
                    "small": "media/small/1514625172-2.jpg",
                    "medium": "media/medium/1514625172-2.jpg",
                    "large": "http://localhost:8000/media/large/1514625172-2.jpg",
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                },
                {
                    "id": 4885,
                    "mime": "image/jpeg",
                    "thumb": "media/thumb/1514625173-3.jpg",
                    "small": "media/small/1514625173-3.jpg",
                    "medium": "media/medium/1514625173-3.jpg",
                    "large": "http://localhost:8000/media/large/1514625173-3.jpg",
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                },
                {
                    "id": 4886,
                    "mime": "image/jpeg",
                    "thumb": "media/thumb/1514625174-4.jpg",
                    "small": "media/small/1514625174-4.jpg",
                    "medium": "media/medium/1514625174-4.jpg",
                    "large": "http://localhost:8000/media/large/1514625174-4.jpg",
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                },
                {
                    "id": 4887,
                    "mime": "image/jpeg",
                    "thumb": "media/thumb/1514625175-5.jpg",
                    "small": "media/small/1514625175-5.jpg",
                    "medium": "media/medium/1514625175-5.jpg",
                    "large": "http://localhost:8000/media/large/1514625175-5.jpg",
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                },
                {
                    "id": 4888,
                    "mime": "image/jpeg",
                    "thumb": "media/thumb/1514625175-6.jpg",
                    "small": "media/small/1514625175-6.jpg",
                    "medium": "media/medium/1514625175-6.jpg",
                    "large": "http://localhost:8000/media/large/1514625175-6.jpg",
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                }
            ]
        }
    },
    "responseMessage": "Product has been successfully Added",
    "responseCode": 200
}


```

<!-- 13 -->

## Delete Product from Cart 


**API** `http://localhost:8000/api/cart/3`

**Method** : DELETE


### Response :


_Example_

```

{
    "cart": {
        "id": 6,
        "user_id": 510,
        "product_id": 1007,
        "quantity": 1,
        "size": null,
        "color": null,
        "status": 1,
        "type": null,
        "created_at": "2018-04-20 08:01:23",
        "updated_at": "2018-04-20 08:01:23"
    },
    "responseCode": 200,
    "responseMessage": "Deleted From Cart"
}


```

<!-- 14 -->

##  View All the cart items of user 


**API** `http://localhost:8000/api/cart/user/510`

**Method** : GET


### Response :


_Example_

```

{
    "cart": [
        {
            "id": 1,
            "user_id": 510,
            "product_id": 1007,
            "quantity": 1,
            "size": null,
            "color": null,
            "status": 1,
            "type": null,
            "created_at": "2018-04-20 07:16:24",
            "updated_at": "2018-04-20 07:16:24",
            "product": {
                "id": 1007,
                "name": "Product",
                "slug": "",
                "bdpin": "",
                "brand_id": 5,
                "model": "xgrfv",
                "sku": "szdgvxdhxd",
                "description": "<p>this is a great product</p>",
                "specification": "rtfgjhnc",
                "weight": "100.00",
                "length": "50.00",
                "width": "2.00",
                "height": "22525.00",
                "amount": "50.00",
                "quantity": 20,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-03-26 12:24:04",
                "updated_at": "2018-04-16 09:05:04",
                "min_price": "100.00",
                "max_price": "1000.00",
                "shipping_charge": "10.00",
                "brand_name": "fhdxcrhgcfgh",
                "brand": {
                    "id": 5,
                    "name": "fhdxcrhgcfgh"
                },
                "organization": {
                    "id": 12,
                    "user_id": 514,
                    "type_id": 0,
                    "name": "bla bla",
                    "logo": "",
                    "gst": "",
                    "incorporation_number": "",
                    "address": "",
                    "introduction": "",
                    "created_at": "2018-03-26 12:22:21",
                    "updated_at": "2018-03-26 12:22:21",
                    "city": "",
                    "state": "",
                    "pincode": "",
                    "country": ""
                }
            },
            "media": [
                {
                    "id": 2,
                    "mime": "",
                    "thumb": "http://lorempixel.com/270/220/business/2",
                    "small": null,
                    "medium": "http://lorempixel.com/480/360/business/2",
                    "large": "http://lorempixel.com/1280/720/business/2",
                    "caption": null,
                    "default": 1,
                    "check": "pending"
                }
            ]
        }
    ],
    "responseMessage": "Successfull",
    "responseCode": 200
}




```

<!-- 15 -->

## Store Cart User Address 


**API** `http://localhost:8000/api/cart/address`

**Method** : POST

### Request :

_Example_

```
{
    "user_id": 510,
    "name" : "sakshi",
    "email" : "yo@gmail.com",
    "mobile" : "1234567890",
    "address" : "tggggawyhrfgbeyshgfraegegea",
    "street" : "10 , 1bgdddddddddddddb",
    "colony" : "uygsfukrg",
    "city"  :"city",
    "state" : "fsuyf",
    "landmark" : "sgfyuesgtes",
    "pincode" : 421848,
    "country" : "India",
    "type" : "shipping"
    
}


```


### Response :


_Example_

```

{
    "user_id": 510,
    "name": "sakshi",
    "email": "yo@gmail.com",
    "mobile": "1234567890",
    "address": "tggggawyhrfgbeyshgfraegegea",
    "street": "10 , 1bgdddddddddddddb",
    "colony": "uygsfukrg",
    "city": “erfer”,
    "state": "fsuyf",
    "landmark": "sgfyuesgtes",
    "pincode": 421848,
    "country": "India",
    "type": "shipping",
    "updated_at": "2018-04-20 11:17:21",
    "created_at": "2018-04-20 11:17:21",
    "id": 1
}




```

<!-- 16 -->

## Add Billing Details or Shipping Detail


**API** `http://localhost:8000/api/cart/address`

**Method** : POST

### Request :

_Example_

```
{
    "user_id": 510,
    "name" : "sakshi",
    "email" : "yo@gmail.com",
    "mobile" : "1234567890",
    "address" : "tggggawyhrfgbeyshgfraegegea",
    "street" : "10 , 1bgdddddddddddddb",
    "colony" : "uygsfukrg",
    "state" : "fsuyf",
    "landmark" : "sgfyuesgtes",
    "pincode" : 421848,
    "country" : "India",
    "type" : "SHIPPING"

}



```


### Response :


_Example_

```

{
    "address": {
        "user_id": 510,
        "name": "sakshi",
        "email": "yo@gmail.com",
        "mobile": "1234567890",
        "address": "tggggawyhrfgbeyshgfraegegea",
        "street": "10 , 1bgdddddddddddddb",
        "colony": "uygsfukrg",
        "city": null,
        "state": "fsuyf",
        "landmark": "sgfyuesgtes",
        "pincode": 421848,
        "country": "India",
        "type": "SHIPPING",
        "updated_at": "2018-04-21 10:28:14",
        "created_at": "2018-04-21 10:28:14",
        "id": 3
    },
    "responseMessage": "Added Successfully",
    "responseCode": 200
}





```



<!-- 17 -->

##  To View Users Billing and Shipping Address



**API** `http://localhost:8000/api/cart/address/510`

**Method** : GET

### Response :


_Example_

```

{
    "shippingAddress": [
        {
            "id": 1,
            "user_id": 510,
            "name": "sakshi",
            "email": "yo@gmail.com",
            "mobile": "1234567890",
            "address": "tggggawyhrfgbeyshgfraegegea",
            "street": "10 , 1bgdddddddddddddb",
            "colony": "uygsfukrg",
            "city": null,
            "state": "fsuyf",
            "landmark": "sgfyuesgtes",
            "pincode": "421848",
            "country": "India",
            "type": "shipping",
            "status": 1,
            "created_at": "2018-04-20 11:17:21",
            "updated_at": "2018-04-20 11:17:21"
        },
        {
            "id": 3,
            "user_id": 510,
            "name": "sakshi",
            "email": "yo@gmail.com",
            "mobile": "1234567890",
            "address": "tggggawyhrfgbeyshgfraegegea",
            "street": "10 , 1bgdddddddddddddb",
            "colony": "uygsfukrg",
            "city": null,
            "state": "fsuyf",
            "landmark": "sgfyuesgtes",
            "pincode": "421848",
            "country": "India",
            "type": "SHIPPING",
            "status": 1,
            "created_at": "2018-04-21 10:28:14",
            "updated_at": "2018-04-21 10:28:14"
        }
    ],
    "responseStatus": 200,
    "responseMessage": "Cart Address Found"
}






```

<!-- 18 -->

##  To Update Users Shipping Address



**API** `http://localhost:8000/api/cart/510/address/3`

**Method** : PUT

### Request :


_Example_
```
{
    "name" : "sanjay",
    "email" : "yo@gmail.com",
    "mobile" : "1234567890",
    "address" : "tggggawyhrfgbeyshgfraegegea",
    "street" : "10 , 1bgdddddddddddddb",
    "colony" : "uygsfukrg",
    "city" : "vbycgsvafyk",
    "state" : "fsuyf",
    "landmark" : "sgfyuesgtes",
    "pincode" : 421848,
    "country" : "India",
    "type" : "SHIPPING"
}
```

### Response

```
{
    "shippingAddress": 1,
    "responseStatus": 200,
    "responseMessage": "Cart Address Updated"
}
```

<!-- 19 -->

##  Delete Users Shipping Address



**API** `http://localhost:8000/api/cart/510/address/3`

**Method** : Delete

### Response :


_Example_

```
{
    "cart": {
        "id": 3,
        "user_id": 510,
        "name": "sanjay",
        "email": "yo@gmail.com",
        "mobile": "1234567890",
        "address": "tggggawyhrfgbeyshgfraegegea",
        "street": "10 , 1bgdddddddddddddb",
        "colony": "uygsfukrg",
        "city": "vbycgsvafyk",
        "state": "fsuyf",
        "landmark": "sgfyuesgtes",
        "pincode": "421848",
        "country": "India",
        "type": "SHIPPING",
        "status": 1,
        "created_at": "2018-04-21 10:28:14",
        "updated_at": "2018-05-05 18:04:47"
    },
    "responseCode": 200,
    "responseMessage": "Address Deleted"
}
```

<!-- 20 -->

##  Create Order


**API** `http://localhost:8000/api/addToOrder/{cart_id}`

**Method** : Post

### Request :


_Example_

```
{
    "quantity": 10,
    "payment_id" : "hvfdxkj",
    "address_id" : 2
}
```

### Response :

```
{
    "order": {
        "user_id": 510,
        "name": "DS_Order_QRSYyjKZGiznuI5H",
        "price": 210,
        "amount": "21.00",
        "status": "placed",
        "payment_method": "COD",
        "updated_at": "2018-05-07 16:56:06",
        "created_at": "2018-05-07 16:56:06",
        "id": 196
    },
    "item": {
        "order_id": 196,
        "product_id": 1011,
        "name": "sZEfgfr",
        "quantity": 10,
        "amount": 50,
        "status": "placed",
        "attribute_id": 17,
        "shipping_charge": "2.00",
        "id": 82
    },
    "payment": true
}
```


<!-- 21 -->

##  Contact Us


**API** `http://localhost:8000/api/contact`

**Method** : Post

### Request :


_Example_

```
{
    "subject" : "sfgsgras",
    "message": "ayhdgef"
}
```


### Response :

```
{
    "subject": "sfgsgras",
    "message": "ayhdgef",
    "email": "client@seller.com",
    "status": "open",
    "updated_at": "2018-05-09 11:50:48",
    "created_at": "2018-05-09 11:50:48",
    "id": 113
}
```

<!-- 22 -->

##  My Orders


**API** `http://localhost:8000/api/orders/user/510`

**Method** : Get

### Response :


_Example_

```
{
    "orders": [
        {
            "id": 264,
            "order_id": "271",
            "product_id": "13",
            "attribute_id": "0",
            "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Blue Color With laptop Compartment",
            "quantity": "1",
            "amount": "449",
            "organization_id": "0",
            "status": "placed",
            "shipment_id": "",
            "shipping_charge": "75.00",
            "order": {
                "id": 271,
                "user_id": "796",
                "client_id": "0",
                "name": "DS_Order_qLvsDGnAyyBqXRM0",
                "invoice": "",
                "amount": "449.00",
                "created_at": "2018-05-10 15:52:41",
                "updated_at": "2018-05-10 15:52:41",
                "status": "placed",
                "price": "449.00",
                "payment_method": "PREPAID"
            },
            "product": {
                "id": 13,
                "user_id": "1",
                "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Blue Color With laptop Compartment",
                "slug": "",
                "bdpin": "",
                "brand_id": "1",
                "model": "BAG15",
                "sku": "BAG15",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "Model Number\tBAG15\r\nItem Height\t15 Centimeters\r\nItem Length\t20 Centimeters\r\nItem Width\t5 Centimeters\r\nVolume Capacity\t20 Liters\r\nItem Weight\t430 Grams\r\nMaterial\tPolyester\r\nSpecial Features\tZip Closure, Shoulder Strap, Laptop Compartment\r\nClosure\tZipper\r\nInner Material\tSatin\r\nStrap\tAdjustable\r\nWarranty Type\tManufacturer",
                "weight": "500.00",
                "length": "40.00",
                "width": "20.00",
                "height": "30.00",
                "amount": "449.00",
                "quantity": "20",
                "status": "1",
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-11-18 13:34:52",
                "updated_at": "2018-05-08 17:32:32",
                "min_price": "449.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "brand_name": "TT BAGS",
                "brand": {
                    "id": 1,
                    "name": "TT BAGS"
                },
                "media": [
                    {
                        "id": 11,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012127-15-1.jpg",
                        "small": "media/small/1511012127-15-1.jpg",
                        "medium": "media/medium/1511012127-15-1.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012127-15-1.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 12,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012127-15-2.jpg",
                        "small": "media/small/1511012127-15-2.jpg",
                        "medium": "media/medium/1511012127-15-2.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012127-15-2.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 13,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012128-15-3.jpg",
                        "small": "media/small/1511012128-15-3.jpg",
                        "medium": "media/medium/1511012128-15-3.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012128-15-3.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 14,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012129-15-4.jpg",
                        "small": "media/small/1511012129-15-4.jpg",
                        "medium": "media/medium/1511012129-15-4.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012129-15-4.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 15,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012130-15-5.jpg",
                        "small": "media/small/1511012130-15-5.jpg",
                        "medium": "media/medium/1511012130-15-5.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012130-15-5.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    }
                ]
            }
        },
        {
            "id": 271,
            "order_id": "278",
            "product_id": "13",
            "attribute_id": "0",
            "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Blue Color With laptop Compartment",
            "quantity": "1",
            "amount": "449",
            "organization_id": "0",
            "status": "placed",
            "shipment_id": "",
            "shipping_charge": "75.00",
            "order": {
                "id": 278,
                "user_id": "796",
                "client_id": "0",
                "name": "DS_Order_C2rwIWm29HhfIphf",
                "invoice": "",
                "amount": "449.00",
                "created_at": "2018-05-14 16:41:08",
                "updated_at": "2018-05-14 16:41:08",
                "status": "placed",
                "price": "449.00",
                "payment_method": "PREPAID"
            },
            "product": {
                "id": 13,
                "user_id": "1",
                "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Blue Color With laptop Compartment",
                "slug": "",
                "bdpin": "",
                "brand_id": "1",
                "model": "BAG15",
                "sku": "BAG15",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "Model Number\tBAG15\r\nItem Height\t15 Centimeters\r\nItem Length\t20 Centimeters\r\nItem Width\t5 Centimeters\r\nVolume Capacity\t20 Liters\r\nItem Weight\t430 Grams\r\nMaterial\tPolyester\r\nSpecial Features\tZip Closure, Shoulder Strap, Laptop Compartment\r\nClosure\tZipper\r\nInner Material\tSatin\r\nStrap\tAdjustable\r\nWarranty Type\tManufacturer",
                "weight": "500.00",
                "length": "40.00",
                "width": "20.00",
                "height": "30.00",
                "amount": "449.00",
                "quantity": "20",
                "status": "1",
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-11-18 13:34:52",
                "updated_at": "2018-05-08 17:32:32",
                "min_price": "449.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "brand_name": "TT BAGS",
                "brand": {
                    "id": 1,
                    "name": "TT BAGS"
                },
                "media": [
                    {
                        "id": 11,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012127-15-1.jpg",
                        "small": "media/small/1511012127-15-1.jpg",
                        "medium": "media/medium/1511012127-15-1.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012127-15-1.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 12,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012127-15-2.jpg",
                        "small": "media/small/1511012127-15-2.jpg",
                        "medium": "media/medium/1511012127-15-2.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012127-15-2.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 13,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012128-15-3.jpg",
                        "small": "media/small/1511012128-15-3.jpg",
                        "medium": "media/medium/1511012128-15-3.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012128-15-3.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 14,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012129-15-4.jpg",
                        "small": "media/small/1511012129-15-4.jpg",
                        "medium": "media/medium/1511012129-15-4.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012129-15-4.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 15,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012130-15-5.jpg",
                        "small": "media/small/1511012130-15-5.jpg",
                        "medium": "media/medium/1511012130-15-5.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012130-15-5.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    }
                ]
            }
        },
        {
            "id": 272,
            "order_id": "279",
            "product_id": "14",
            "attribute_id": "0",
            "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Green Color With laptop Compartment",
            "quantity": "1",
            "amount": "449",
            "organization_id": "0",
            "status": "placed",
            "shipment_id": "",
            "shipping_charge": "75.00",
            "order": {
                "id": 279,
                "user_id": "796",
                "client_id": "0",
                "name": "DS_Order_DhClmjWTAIaDboOY",
                "invoice": "",
                "amount": "449.00",
                "created_at": "2018-05-14 16:43:21",
                "updated_at": "2018-05-14 16:43:21",
                "status": "placed",
                "price": "449.00",
                "payment_method": "PREPAID"
            },
            "product": {
                "id": 14,
                "user_id": "1",
                "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Green Color With laptop Compartment",
                "slug": "",
                "bdpin": "",
                "brand_id": "1",
                "model": "BAG16",
                "sku": "BAG16",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "Model Number\tBAG16\r\nItem Height\t15 Centimeters\r\nItem Length\t20 Centimeters\r\nItem Width\t5 Centimeters\r\nVolume Capacity\t20 Liters\r\nItem Weight\t430 Grams\r\nMaterial\tPolyester\r\nSpecial Features\tZip Closure, Shoulder Strap, Laptop Compartment\r\nClosure\tZipper\r\nInner Material\tSatin\r\nStrap\tAdjustable\r\nWarranty Type\tManufacturer",
                "weight": "500.00",
                "length": "40.00",
                "width": "20.00",
                "height": "30.00",
                "amount": "449.00",
                "quantity": "20",
                "status": "1",
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-11-18 13:39:41",
                "updated_at": "2018-05-08 17:32:26",
                "min_price": "449.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "brand_name": "TT BAGS",
                "brand": {
                    "id": 1,
                    "name": "TT BAGS"
                },
                "media": [
                    {
                        "id": 16,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012497-16-1.jpg",
                        "small": "media/small/1511012497-16-1.jpg",
                        "medium": "media/medium/1511012497-16-1.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012497-16-1.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 17,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012498-16-2.jpg",
                        "small": "media/small/1511012498-16-2.jpg",
                        "medium": "media/medium/1511012498-16-2.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012498-16-2.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 18,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012498-16-3.jpg",
                        "small": "media/small/1511012498-16-3.jpg",
                        "medium": "media/medium/1511012498-16-3.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012498-16-3.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 19,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012499-16-4.jpg",
                        "small": "media/small/1511012499-16-4.jpg",
                        "medium": "media/medium/1511012499-16-4.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012499-16-4.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 20,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012500-16-5.jpg",
                        "small": "media/small/1511012500-16-5.jpg",
                        "medium": "media/medium/1511012500-16-5.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012500-16-5.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    }
                ]
            }
        },
        {
            "id": 277,
            "order_id": "289",
            "product_id": "13",
            "attribute_id": "0",
            "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Blue Color With laptop Compartment",
            "quantity": "1",
            "amount": "449",
            "organization_id": "0",
            "status": "placed",
            "shipment_id": "",
            "shipping_charge": "75.00",
            "order": {
                "id": 289,
                "user_id": "796",
                "client_id": "0",
                "name": "DS_Order_Nuuun7WGOdBzu6Us",
                "invoice": "",
                "amount": "449.00",
                "created_at": "2018-05-17 11:50:25",
                "updated_at": "2018-05-17 11:50:25",
                "status": "placed",
                "price": "449.00",
                "payment_method": "PREPAID"
            },
            "product": {
                "id": 13,
                "user_id": "1",
                "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Blue Color With laptop Compartment",
                "slug": "",
                "bdpin": "",
                "brand_id": "1",
                "model": "BAG15",
                "sku": "BAG15",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "Model Number\tBAG15\r\nItem Height\t15 Centimeters\r\nItem Length\t20 Centimeters\r\nItem Width\t5 Centimeters\r\nVolume Capacity\t20 Liters\r\nItem Weight\t430 Grams\r\nMaterial\tPolyester\r\nSpecial Features\tZip Closure, Shoulder Strap, Laptop Compartment\r\nClosure\tZipper\r\nInner Material\tSatin\r\nStrap\tAdjustable\r\nWarranty Type\tManufacturer",
                "weight": "500.00",
                "length": "40.00",
                "width": "20.00",
                "height": "30.00",
                "amount": "449.00",
                "quantity": "20",
                "status": "1",
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-11-18 13:34:52",
                "updated_at": "2018-05-08 17:32:32",
                "min_price": "449.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "brand_name": "TT BAGS",
                "brand": {
                    "id": 1,
                    "name": "TT BAGS"
                },
                "media": [
                    {
                        "id": 11,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012127-15-1.jpg",
                        "small": "media/small/1511012127-15-1.jpg",
                        "medium": "media/medium/1511012127-15-1.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012127-15-1.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 12,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012127-15-2.jpg",
                        "small": "media/small/1511012127-15-2.jpg",
                        "medium": "media/medium/1511012127-15-2.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012127-15-2.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 13,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012128-15-3.jpg",
                        "small": "media/small/1511012128-15-3.jpg",
                        "medium": "media/medium/1511012128-15-3.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012128-15-3.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 14,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012129-15-4.jpg",
                        "small": "media/small/1511012129-15-4.jpg",
                        "medium": "media/medium/1511012129-15-4.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012129-15-4.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 15,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012130-15-5.jpg",
                        "small": "media/small/1511012130-15-5.jpg",
                        "medium": "media/medium/1511012130-15-5.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012130-15-5.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    }
                ]
            }
        },
        {
            "id": 278,
            "order_id": "290",
            "product_id": "13",
            "attribute_id": "0",
            "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Blue Color With laptop Compartment",
            "quantity": "1",
            "amount": "449",
            "organization_id": "0",
            "status": "placed",
            "shipment_id": "",
            "shipping_charge": "75.00",
            "order": {
                "id": 290,
                "user_id": "796",
                "client_id": "0",
                "name": "DS_Order_gGvEEHLHzHt5G4BW",
                "invoice": "",
                "amount": "449.00",
                "created_at": "2018-05-17 11:54:26",
                "updated_at": "2018-05-17 11:54:26",
                "status": "placed",
                "price": "449.00",
                "payment_method": "PREPAID"
            },
            "product": {
                "id": 13,
                "user_id": "1",
                "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Blue Color With laptop Compartment",
                "slug": "",
                "bdpin": "",
                "brand_id": "1",
                "model": "BAG15",
                "sku": "BAG15",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "Model Number\tBAG15\r\nItem Height\t15 Centimeters\r\nItem Length\t20 Centimeters\r\nItem Width\t5 Centimeters\r\nVolume Capacity\t20 Liters\r\nItem Weight\t430 Grams\r\nMaterial\tPolyester\r\nSpecial Features\tZip Closure, Shoulder Strap, Laptop Compartment\r\nClosure\tZipper\r\nInner Material\tSatin\r\nStrap\tAdjustable\r\nWarranty Type\tManufacturer",
                "weight": "500.00",
                "length": "40.00",
                "width": "20.00",
                "height": "30.00",
                "amount": "449.00",
                "quantity": "20",
                "status": "1",
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-11-18 13:34:52",
                "updated_at": "2018-05-08 17:32:32",
                "min_price": "449.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "brand_name": "TT BAGS",
                "brand": {
                    "id": 1,
                    "name": "TT BAGS"
                },
                "media": [
                    {
                        "id": 11,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012127-15-1.jpg",
                        "small": "media/small/1511012127-15-1.jpg",
                        "medium": "media/medium/1511012127-15-1.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012127-15-1.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 12,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012127-15-2.jpg",
                        "small": "media/small/1511012127-15-2.jpg",
                        "medium": "media/medium/1511012127-15-2.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012127-15-2.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 13,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012128-15-3.jpg",
                        "small": "media/small/1511012128-15-3.jpg",
                        "medium": "media/medium/1511012128-15-3.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012128-15-3.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 14,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012129-15-4.jpg",
                        "small": "media/small/1511012129-15-4.jpg",
                        "medium": "media/medium/1511012129-15-4.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012129-15-4.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 15,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012130-15-5.jpg",
                        "small": "media/small/1511012130-15-5.jpg",
                        "medium": "media/medium/1511012130-15-5.jpg",
                        "large": "http://dropship.bigly.io/media/large/1511012130-15-5.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    }
                ]
            }
        },
        {
            "id": 281,
            "order_id": "293",
            "product_id": "22937",
            "attribute_id": "0",
            "name": "Desigrace Small Belt Palazzo- Beige",
            "quantity": "10",
            "amount": "275",
            "organization_id": "0",
            "status": "placed",
            "shipment_id": "",
            "shipping_charge": "75.00",
            "order": {
                "id": 293,
                "user_id": "796",
                "client_id": "0",
                "name": "DS_Order_kskg32FqpmyvJaTF",
                "invoice": "",
                "amount": "275.00",
                "created_at": "2018-05-17 13:21:59",
                "updated_at": "2018-05-17 13:21:59",
                "status": "placed",
                "price": "2750.00",
                "payment_method": "COD"
            },
            "product": {
                "id": 22937,
                "user_id": "830",
                "name": "Desigrace Small Belt Palazzo- Beige",
                "slug": "",
                "bdpin": "",
                "brand_id": "197",
                "model": " DG12005001",
                "sku": " DG12005001",
                "description": "Desigrace Presents the design High Quality Multi color jegging/ Casual Tousers/Plazzo/Legging/Salwar/Tuning Top For Beautiful Girls. It Comes In jegging Pattern Which Makes It More Beautiful. It'S Made Of Lycra Stuff And Superior In Quality, Marvellous And Style In Design. It'S a Multi Coloured Apparel. It Is Revealing Attire Which Looks Gorgeous On The Body To Enjoy Beautiful Moments With Beloved Ones. You Can Club These jegging With Any Stylish Trouser. Print Sequence Might Slightly Differ, You Will Get Almost Similar Product.",
                "specification": "Specialty : Unique Design , Production place : Made in India",
                "weight": "350.00",
                "length": "20.00",
                "width": "0.20",
                "height": "25.00",
                "amount": "275.00",
                "quantity": "25",
                "status": "1",
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-04-26 15:35:45",
                "updated_at": "2018-04-26 15:35:45",
                "min_price": "275.00",
                "max_price": "699.00",
                "shipping_charge": "75.00",
                "brand_name": "Desigrace",
                "brand": {
                    "id": 197,
                    "name": "Desigrace"
                },
                "media": [
                    {
                        "id": 66757,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740554-6o9a5084.jpg",
                        "small": "http://s.bigly.io/products/small/1524740554-6o9a5084.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740554-6o9a5084.jpg",
                        "large": "http://s.bigly.io/products/large/1524740554-6o9a5084.jpg",
                        "caption": null,
                        "default": "1",
                        "check": "pending"
                    },
                    {
                        "id": 66758,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740556-6o9a5086.jpg",
                        "small": "http://s.bigly.io/products/small/1524740556-6o9a5086.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740556-6o9a5086.jpg",
                        "large": "http://s.bigly.io/products/large/1524740556-6o9a5086.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66759,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740557-6o9a5087.jpg",
                        "small": "http://s.bigly.io/products/small/1524740557-6o9a5087.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740557-6o9a5087.jpg",
                        "large": "http://s.bigly.io/products/large/1524740557-6o9a5087.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66760,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740558-6o9a5088.jpg",
                        "small": "http://s.bigly.io/products/small/1524740558-6o9a5088.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740558-6o9a5088.jpg",
                        "large": "http://s.bigly.io/products/large/1524740558-6o9a5088.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66761,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740559-6o9a5089.jpg",
                        "small": "http://s.bigly.io/products/small/1524740559-6o9a5089.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740559-6o9a5089.jpg",
                        "large": "http://s.bigly.io/products/large/1524740559-6o9a5089.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66762,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740560-6o9a5090.jpg",
                        "small": "http://s.bigly.io/products/small/1524740560-6o9a5090.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740560-6o9a5090.jpg",
                        "large": "http://s.bigly.io/products/large/1524740560-6o9a5090.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66763,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740562-6o9a5091.jpg",
                        "small": "http://s.bigly.io/products/small/1524740562-6o9a5091.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740562-6o9a5091.jpg",
                        "large": "http://s.bigly.io/products/large/1524740562-6o9a5091.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    }
                ]
            }
        },
        {
            "id": 282,
            "order_id": "294",
            "product_id": "22936",
            "attribute_id": "0",
            "name": "Desigrace Double Miyani Legging- Red",
            "quantity": "1",
            "amount": "180",
            "organization_id": "0",
            "status": "placed",
            "shipment_id": "",
            "shipping_charge": "75.00",
            "order": {
                "id": 294,
                "user_id": "796",
                "client_id": "0",
                "name": "DS_Order_z0z27ZAyFXBNESif",
                "invoice": "",
                "amount": "180.00",
                "created_at": "2018-05-17 13:24:18",
                "updated_at": "2018-05-17 13:24:18",
                "status": "placed",
                "price": "180.00",
                "payment_method": "COD"
            },
            "product": {
                "id": 22936,
                "user_id": "830",
                "name": "Desigrace Double Miyani Legging- Red",
                "slug": "",
                "bdpin": "",
                "brand_id": "197",
                "model": " DG11005028",
                "sku": " DG11005028",
                "description": "Desigrace Presents the design High Quality Multi color jegging/ Casual Tousers/Plazzo/Legging/Salwar/Tuning Top For Beautiful Girls. It Comes In jegging Pattern Which Makes It More Beautiful. It'S Made Of Lycra Stuff And Superior In Quality, Marvellous And Style In Design. It'S a Multi Coloured Apparel. It Is Revealing Attire Which Looks Gorgeous On The Body To Enjoy Beautiful Moments With Beloved Ones. You Can Club These jegging With Any Stylish Trouser. Print Sequence Might Slightly Differ, You Will Get Almost Similar Product.",
                "specification": "Specialty : (No color fade), Production place : Made in India",
                "weight": "350.00",
                "length": "20.00",
                "width": "0.20",
                "height": "25.00",
                "amount": "180.00",
                "quantity": "25",
                "status": "1",
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-04-26 15:35:45",
                "updated_at": "2018-04-26 15:35:45",
                "min_price": "180.00",
                "max_price": "499.00",
                "shipping_charge": "75.00",
                "brand_name": "Desigrace",
                "brand": {
                    "id": 197,
                    "name": "Desigrace"
                },
                "media": [
                    {
                        "id": 66764,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740750-71.jpg",
                        "small": "http://s.bigly.io/products/small/1524740750-71.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740750-71.jpg",
                        "large": "http://s.bigly.io/products/large/1524740750-71.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66765,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740751-72.jpg",
                        "small": "http://s.bigly.io/products/small/1524740751-72.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740751-72.jpg",
                        "large": "http://s.bigly.io/products/large/1524740751-72.jpg",
                        "caption": null,
                        "default": "1",
                        "check": "pending"
                    },
                    {
                        "id": 66766,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740752-74.jpg",
                        "small": "http://s.bigly.io/products/small/1524740752-74.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740752-74.jpg",
                        "large": "http://s.bigly.io/products/large/1524740752-74.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66767,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740752-75.jpg",
                        "small": "http://s.bigly.io/products/small/1524740752-75.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740752-75.jpg",
                        "large": "http://s.bigly.io/products/large/1524740752-75.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    }
                ]
            }
        },
        {
            "id": 283,
            "order_id": "295",
            "product_id": "22937",
            "attribute_id": "0",
            "name": "Desigrace Small Belt Palazzo- Beige",
            "quantity": "10",
            "amount": "275",
            "organization_id": "0",
            "status": "cancelled",
            "shipment_id": "",
            "shipping_charge": "75.00",
            "order": {
                "id": 295,
                "user_id": "796",
                "client_id": "0",
                "name": "DS_Order_XXotipU2AyvM2SVZ",
                "invoice": "",
                "amount": "275.00",
                "created_at": "2018-05-17 13:30:06",
                "updated_at": "2018-05-17 13:36:33",
                "status": "cancelled",
                "price": "2750.00",
                "payment_method": "COD"
            },
            "product": {
                "id": 22937,
                "user_id": "830",
                "name": "Desigrace Small Belt Palazzo- Beige",
                "slug": "",
                "bdpin": "",
                "brand_id": "197",
                "model": " DG12005001",
                "sku": " DG12005001",
                "description": "Desigrace Presents the design High Quality Multi color jegging/ Casual Tousers/Plazzo/Legging/Salwar/Tuning Top For Beautiful Girls. It Comes In jegging Pattern Which Makes It More Beautiful. It'S Made Of Lycra Stuff And Superior In Quality, Marvellous And Style In Design. It'S a Multi Coloured Apparel. It Is Revealing Attire Which Looks Gorgeous On The Body To Enjoy Beautiful Moments With Beloved Ones. You Can Club These jegging With Any Stylish Trouser. Print Sequence Might Slightly Differ, You Will Get Almost Similar Product.",
                "specification": "Specialty : Unique Design , Production place : Made in India",
                "weight": "350.00",
                "length": "20.00",
                "width": "0.20",
                "height": "25.00",
                "amount": "275.00",
                "quantity": "25",
                "status": "1",
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-04-26 15:35:45",
                "updated_at": "2018-04-26 15:35:45",
                "min_price": "275.00",
                "max_price": "699.00",
                "shipping_charge": "75.00",
                "brand_name": "Desigrace",
                "brand": {
                    "id": 197,
                    "name": "Desigrace"
                },
                "media": [
                    {
                        "id": 66757,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740554-6o9a5084.jpg",
                        "small": "http://s.bigly.io/products/small/1524740554-6o9a5084.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740554-6o9a5084.jpg",
                        "large": "http://s.bigly.io/products/large/1524740554-6o9a5084.jpg",
                        "caption": null,
                        "default": "1",
                        "check": "pending"
                    },
                    {
                        "id": 66758,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740556-6o9a5086.jpg",
                        "small": "http://s.bigly.io/products/small/1524740556-6o9a5086.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740556-6o9a5086.jpg",
                        "large": "http://s.bigly.io/products/large/1524740556-6o9a5086.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66759,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740557-6o9a5087.jpg",
                        "small": "http://s.bigly.io/products/small/1524740557-6o9a5087.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740557-6o9a5087.jpg",
                        "large": "http://s.bigly.io/products/large/1524740557-6o9a5087.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66760,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740558-6o9a5088.jpg",
                        "small": "http://s.bigly.io/products/small/1524740558-6o9a5088.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740558-6o9a5088.jpg",
                        "large": "http://s.bigly.io/products/large/1524740558-6o9a5088.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66761,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740559-6o9a5089.jpg",
                        "small": "http://s.bigly.io/products/small/1524740559-6o9a5089.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740559-6o9a5089.jpg",
                        "large": "http://s.bigly.io/products/large/1524740559-6o9a5089.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66762,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740560-6o9a5090.jpg",
                        "small": "http://s.bigly.io/products/small/1524740560-6o9a5090.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740560-6o9a5090.jpg",
                        "large": "http://s.bigly.io/products/large/1524740560-6o9a5090.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    },
                    {
                        "id": 66763,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/1524740562-6o9a5091.jpg",
                        "small": "http://s.bigly.io/products/small/1524740562-6o9a5091.jpg",
                        "medium": "http://s.bigly.io/products/medium/1524740562-6o9a5091.jpg",
                        "large": "http://s.bigly.io/products/large/1524740562-6o9a5091.jpg",
                        "caption": null,
                        "default": "0",
                        "check": "pending"
                    }
                ]
            }
        }
    ],
    "responseMessage": "User All Orders",
    "responseCode": 200
}
```



<!-- 23 -->

##  Orders Details


**API** `http://localhost:8000/api/orders/199`

**Method** : Get

### Response :


_Example_

```
{
    "order_detail": {
        "id": 314,
        "order_id": 326,
        "product_id": 12583,
        "attribute_id": 0,
        "name": "General Knowledge 2019",
        "quantity": 1,
        "amount": 20,
        "organization_id": 219,
        "status": "delivered",
        "shipment_id": "441188326",
        "shipping_charge": "30.00",
        "product": {
            "id": 12583,
            "user_id": 254,
            "name": "General Knowledge 2019",
            "slug": "",
            "bdpin": "",
            "brand_id": 57,
            "model": "BDPIN10003",
            "sku": "BDPIN10003",
            "description": "\r\n\r\nGeneral Knowledge is the steady awareness towards progress of one’s surroundings. Building knowledge of all significant events and happenings requires consistency in learning on day to day basis and has also become essential for success in all competitions. General knowledge 2019 by Manohar Pandey comes as a comprehensive assimilation of factual information which proves useful for the aspirants of SSC, Bank, Railway, Police, NDA/CDS and Other Exams. With extensive coverage on current affairs, the book presents facts and figures with appropriate use of pictograms, graphics and tables for Simplified Learning and Easy Grasping. The syllabus for General Knowledge is broad and undefined and requires accurate, complete, topical coverage of facts from all walks of life.Covered in 5 chapters, one for each discipline, the book is a reliable and recommended source of information for anyone appearing in the forthcoming competitive exams.Table of ContentsCurrent AffairsHistory, Geography, Indian Polity, Indian Economy, General Science.\r\n\r\n",
            "specification": "\r\n\r\nPaperback:&nbsp;160 pagesPublisher:&nbsp;Arihant Publications; Eleventh edition (2018)Language:&nbsp;English\r\n\r\n",
            "weight": "100.00",
            "length": "20.00",
            "width": "0.60",
            "height": "13.00",
            "amount": "20.00",
            "quantity": 124,
            "status": 1,
            "source": "bigly",
            "source_id": null,
            "created_at": "2018-02-20 15:49:34",
            "updated_at": "2018-05-30 17:27:28",
            "min_price": "20.00",
            "max_price": "50.00",
            "shipping_charge": "30.00",
            "brand_name": "By Manohar Pandey",
            "brand": {
                "id": 57,
                "name": "By Manohar Pandey"
            },
            "media": [
                {
                    "id": 27558,
                    "mime": "image/jpeg",
                    "thumb": "http://s.bigly.io/products/thumb/1519121995-41cme4z8c.jpg",
                    "small": "http://s.bigly.io/products/small/1519121995-41cme4z8c.jpg",
                    "medium": "http://s.bigly.io/products/medium/1519121995-41cme4z8c.jpg",
                    "large": "http://s.bigly.io/products/large/1519121995-41cme4z8c.jpg",
                    "caption": null,
                    "default": 1,
                    "check": "pending"
                }
            ]
        },
        "order": {
            "id": 326,
            "user_id": 989,
            "client_id": 0,
            "name": "DS_Order_j2rw1ksgIo0Nw6xV",
            "invoice": "",
            "amount": "20.00",
            "created_at": "2018-05-30 12:11:47",
            "updated_at": "2018-05-30 12:11:47",
            "status": "placed",
            "price": "20.00",
            "payment_method": "PREPAID"
        },
        "attribute_data": null,
        "organization": {
            "id": 219,
            "name": "Forbidden Retail"
        }
    },
    "shipping_address": {
        "id": 55,
        "user_id": 989,
        "order_id": 326,
        "name": "Gunjan",
        "email": null,
        "mobile": "7290918926",
        "address": "gaya",
        "street": "gzhzg",
        "colony": "gzhzg",
        "city": "New Dehi",
        "state": "Bihar",
        "landmark": "vzhsj",
        "pincode": "9865325",
        "country": "INDIA",
        "type": "BILLING",
        "status": 1,
        "created_at": "2018-05-30 12:11:47",
        "updated_at": "2018-05-30 12:11:47"
    },
    "responseMessage": "Order Detail",
    "responseCode": 200
}

```



<!-- 24 -->

##  Cancel Reason


**API** `http://localhost:8000/api/reason`

**Method** : Get

### Response :


_Example_

```
{
    "reasons": [
        {
            "id": 1,
            "reason": "rdetjdrf6jureu"
        },
        {
            "id": 2,
            "reason": "this is my reason"
        }
    ]
}
```




<!-- 25 -->

##  Cancel Order


**API** `http://dropship.bigly.io/api/orderCancel/271`

**Method** : Post

### Request :


_Example_

```
{
    "reason_id" : 2,
    "reason" : "Reason Text"
}

```

### Response

```
{
    "order": {
        "id": 271,
        "user_id": "796",
        "client_id": "0",
        "name": "DS_Order_qLvsDGnAyyBqXRM0",
        "invoice": "",
        "amount": "449.00",
        "created_at": "2018-05-10 15:52:41",
        "updated_at": "2018-05-18 12:19:37",
        "status": "cancelled",
        "price": "449.00",
        "payment_method": "PREPAID"
    },
    "reason": {
        "user_id": 796,
        "order_id": "271",
        "reason": "this is reason 2",
        "user_type": "client",
        "reason_type": 2,
        "type": "orders",
        "updated_at": "2018-05-18 12:20:07",
        "created_at": "2018-05-18 12:20:07",
        "id": 7
    },
    "responseMessage": "Order Cancelled",
}
```


<!-- 26 -->

## My Profile 

**API** `http://localhost:8000/api/user`

**Method** : Get

### Response

```

{
    "user": {
        "id": 759,
        "name": "sakshi",
        "username": null,
        "email": "sakshikbc@gmail.com",
        "status": 1,
        "phone": null,
        "created_at": "Apr 13, 2018",
        "updated_at": "2018-05-19 18:09:33",
        "type": "client"
    },
    "address": {
        "id": 25,
        "user_id": 759,
        "order_id": 0,
        "name": "sakshi",
        "email": "sakshikbc@gmail.com",
        "mobile": null,
        "address": "tggggawyhrfgbeyshgfraegegea",
        "street": "10 , 1bgdddddddddddddb",
        "colony": "uygsfukrg",
        "city": "vbycgsvafyk",
        "state": "fsuyf",
        "landmark": "sgfyuesgtes",
        "pincode": "421848",
        "country": "India",
        "type": "BILLING",
        "status": 1,
        "created_at": "2018-05-19 18:09:33",
        "updated_at": "2018-05-19 18:09:33"
    }
}

```


<!-- 27 -->

## Edit Profile 

**API** `http://localhost:8000/api/user/510/edit`

**Method** : Get


### Response

```

{
    "id": 510,
    "name": "client",
    "username": null,
    "email": "client@seller.com",
    "status": 1,
    "phone": "1234567890",
    "created_at": "Mar 03, 2018",
    "updated_at": "2018-03-03 07:23:29",
    "type": "client"
}

```


<!-- 28 -->

## Update Profile 

**API** `http://localhost:8000/api/user/510/update`

**Method** : Post


### Request

```
{
    "name" : "sakshi",
    "email" : "yo@gmail.com",
    "mobile" : "1234567890",
    "address" : "tggggawyhrfgbeyshgfraegegea",
    "street" : "10 , 1bgdddddddddddddb",
    "colony" : "uygsfukrg",
    "city" : "vbycgsvafyk",
    "state" : "fsuyf",
    "landmark" : "sgfyuesgtes",
    "pincode" : 421848,
    "country" : "India",
    "type" : "BILLING"

}

```


### Response

```
{
    "user": {
        "id": 759,
        "name": "sakshi",
        "username": null,
        "email": "sakshikbc@gmail.com",
        "status": 1,
        "phone": null,
        "created_at": "Apr 13, 2018",
        "updated_at": "2018-05-19 18:09:33",
        "type": "client"
    },
    "address": {
        "id": 25,
        "user_id": 759,
        "order_id": 0,
        "name": "sakshi",
        "email": "sakshikbc@gmail.com",
        "mobile": null,
        "address": "tggggawyhrfgbeyshgfraegegea",
        "street": "10 , 1bgdddddddddddddb",
        "colony": "uygsfukrg",
        "city": "vbycgsvafyk",
        "state": "fsuyf",
        "landmark": "sgfyuesgtes",
        "pincode": "421848",
        "country": "India",
        "type": "BILLING",
        "status": 1,
        "created_at": "2018-05-19 18:09:33",
        "updated_at": "2018-05-19 18:09:33"
    }
}
```

<!-- 29 -->

## User Wishlist

**API** `http://dropship.bigly.io/api/userWishlist`

**Method** : Get


### Response

```
{
    "products": {
        "current_page": 1,
        "data": [
            {
                "id": 1,
                "user_id": 1,
                "name": "cfdsgvd",
                "slug": "",
                "bdpin": "1b2327d1-313d-368b-bd91-0638931d5ff5",
                "brand_id": null,
                "model": null,
                "sku": "6b9390ec-1992-3bcb-b658-5743a401ca9c",
                "description": "There was a long tail, certainly,' said Alice, swallowing down her anger as well as if nothing had happened. 'How am I then? Tell me that first, and then, and holding it to be found: all she could.",
                "specification": "",
                "weight": "5904.00",
                "length": "5079.00",
                "width": "8730.00",
                "height": "3265.00",
                "amount": "37.00",
                "quantity": 0,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-03-01 10:54:50",
                "updated_at": "2018-04-06 10:09:16",
                "min_price": "0.00",
                "max_price": "0.00",
                "shipping_charge": "0.00",
                "attributes": [],
                "brand_name": "",
                "organization": {
                    "id": 2,
                    "user_id": 2,
                    "type_id": 0,
                    "name": "Ederno",
                    "logo": "http://s.bigly.io/logo/1520848354-mEbtXPl2agzy9vz.jpg",
                    "gst": "",
                    "incorporation_number": "",
                    "address": "N 21 , Above United Bank of India",
                    "introduction": "",
                    "created_at": "2018-03-01 07:36:47",
                    "updated_at": "2018-03-14 10:14:17",
                    "city": "Satna",
                    "state": "Madhya Pradesh",
                    "pincode": "485001",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 2,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/business/2",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/business/2",
                        "large": "http://lorempixel.com/1280/720/business/2",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 38,
                        "name": "Keebler-Huels",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 17,
                        "name": "Denesik-Ondricka",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 28,
                        "name": "Lubowitz Group",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ]
            },
            {
                "id": 11,
                "user_id": 1,
                "name": "Bergnaum-Watsica",
                "slug": "",
                "bdpin": "28cdf437-98d1-3fa8-983b-4776a00a76b3",
                "brand_id": null,
                "model": null,
                "sku": "051c0184-e905-31ad-bfd9-35245869b9ca",
                "description": "She is such a subject! Our family always HATED cats: nasty, low, vulgar things! Don't let him know she liked them best, For this must ever be A secret, kept from all the creatures wouldn't be so.",
                "specification": "",
                "weight": "6396.00",
                "length": "251.00",
                "width": "8996.00",
                "height": "8259.00",
                "amount": "43.00",
                "quantity": 0,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-03-01 10:54:50",
                "updated_at": "2018-03-01 10:54:50",
                "min_price": "0.00",
                "max_price": "0.00",
                "shipping_charge": "0.00",
                "attributes": [],
                "brand_name": "",
                "organization": null,
                "media": [
                    {
                        "id": 42,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/food/2",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/food/2",
                        "large": "http://lorempixel.com/1280/720/food/2",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 43,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/people/2",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/people/2",
                        "large": "http://lorempixel.com/1280/720/people/2",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 44,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nature/2",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nature/2",
                        "large": "http://lorempixel.com/1280/720/nature/2",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 19,
                        "name": "Carroll-Swaniawski",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 42,
                        "name": "Spencer Group",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ]
            },
            {
                "id": 1011,
                "user_id": 2,
                "name": "sZEfgfr",
                "slug": "",
                "bdpin": "",
                "brand_id": 9,
                "model": "sdgdsgsd",
                "sku": "sdxg",
                "description": "jhgjhg",
                "specification": "srgsde",
                "weight": "15.00",
                "length": "55.00",
                "width": "55.00",
                "height": "5.00",
                "amount": "21.00",
                "quantity": 533,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-05-02 18:11:59",
                "updated_at": "2018-05-18 12:52:17",
                "min_price": "121.00",
                "max_price": "1200.00",
                "shipping_charge": "2.00",
                "attributes": [
                    {
                        "id": 16,
                        "value": "0000FF",
                        "quantity": null,
                        "price": null,
                        "name": "color",
                        "attr_id": 2,
                        "children": [
                            {
                                "id": 17,
                                "value": "50",
                                "quantity": 20,
                                "price": null,
                                "attr_id": 3,
                                "name": "size"
                            }
                        ]
                    }
                ],
                "brand_name": "dsgesdge",
                "organization": {
                    "id": 2,
                    "user_id": 2,
                    "type_id": 0,
                    "name": "Ederno",
                    "logo": "http://s.bigly.io/logo/1520848354-mEbtXPl2agzy9vz.jpg",
                    "gst": "",
                    "incorporation_number": "",
                    "address": "N 21 , Above United Bank of India",
                    "introduction": "",
                    "created_at": "2018-03-01 07:36:47",
                    "updated_at": "2018-03-14 10:14:17",
                    "city": "Satna",
                    "state": "Madhya Pradesh",
                    "pincode": "485001",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 4683,
                        "mime": "image/jpeg",
                        "thumb": "http://s.bigly.io/products/thumb/zkqr1y4lujen9ks-9htf1uw.jpg",
                        "small": "http://s.bigly.io/products/small/zkqr1y4lujen9ks-9htf1uw.jpg",
                        "medium": "http://s.bigly.io/products/medium/zkqr1y4lujen9ks-9htf1uw.jpg",
                        "large": "http://s.bigly.io/products/large/zkqr1y4lujen9ks-9htf1uw.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": []
            }
        ],
        "from": 1,
        "last_page": 1,
        "next_page_url": null,
        "path": "http://localhost:8000/api/userWishlist",
        "per_page": 15,
        "prev_page_url": null,
        "to": 3,
        "total": 3
    },
    "reponse_message": "wishlist found"
}
```

<!-- 30 -->

## Get Faqs

**API** `http://dropship.bigly.io/api/faqs`

**Method** : Get


### Response

```
{
    "data": [
        {
            "que": "What is Bigly",
            "ans": "BigLy is Ecommerce platform tool"
        },
        {
            "que": "What is pricing",
            "ans": "Goto app.bigly.io/pricing to check pricing"
        }
    ]
}
```




<!-- 31-->

## Update Faqs

**API** `http://dropship.bigly.io/api/updateFaq`

**Method** : Post


### Response

```
{
    "data": [
        {
            "que": "What is Bigly",
            "ans": "BigLy is Ecommerce platform tool"
        },
        {
            "que": "What is pricing",
            "ans": "Goto app.bigly.io/pricing to check pricing"
        }
    ]
}
```

<!-- 31 -->



##  All Notifications

**API** `http://localhost:8000/api/notifications`

**Method** : Get

### Response :

_Example_

```
{
    "notifications": [
        {
            "id": 4880,
            "user_id": 989,
            "message_id": 3020,
            "status": "unseen",
            "created_at": "2018-05-30 16:12:27",
            "updated_at": "2018-05-30 16:12:27",
            "type": null,
            "message": {
                "id": 3020,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       70 to 72 .<br>Thankyou",
                "created_at": "2018-05-30 16:12:27",
                "updated_at": "2018-05-30 16:12:27",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 4930,
            "user_id": 989,
            "message_id": 3070,
            "status": "unseen",
            "created_at": "2018-05-30 16:16:38",
            "updated_at": "2018-05-30 16:16:38",
            "type": null,
            "message": {
                "id": 3070,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       75 to 78 .<br>Thankyou",
                "created_at": "2018-05-30 16:16:38",
                "updated_at": "2018-05-30 16:16:38",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 4961,
            "user_id": 989,
            "message_id": 3101,
            "status": "unseen",
            "created_at": "2018-05-30 16:18:47",
            "updated_at": "2018-05-30 16:18:47",
            "type": null,
            "message": {
                "id": 3101,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       78 to 80 .<br>Thankyou",
                "created_at": "2018-05-30 16:18:47",
                "updated_at": "2018-05-30 16:18:47",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 4992,
            "user_id": 989,
            "message_id": 3132,
            "status": "unseen",
            "created_at": "2018-05-30 17:07:44",
            "updated_at": "2018-05-30 17:07:44",
            "type": null,
            "message": {
                "id": 3132,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       80 to 82 .<br>Thankyou",
                "created_at": "2018-05-30 17:07:44",
                "updated_at": "2018-05-30 17:07:44",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5023,
            "user_id": 989,
            "message_id": 3163,
            "status": "unseen",
            "created_at": "2018-05-30 17:08:36",
            "updated_at": "2018-05-30 17:08:36",
            "type": null,
            "message": {
                "id": 3163,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       82 to 85 .<br>Thankyou",
                "created_at": "2018-05-30 17:08:36",
                "updated_at": "2018-05-30 17:08:36",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5054,
            "user_id": 989,
            "message_id": 3194,
            "status": "unseen",
            "created_at": "2018-05-30 17:10:32",
            "updated_at": "2018-05-30 17:10:32",
            "type": null,
            "message": {
                "id": 3194,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       85 to 88 .<br>Thankyou",
                "created_at": "2018-05-30 17:10:32",
                "updated_at": "2018-05-30 17:10:32",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5085,
            "user_id": 989,
            "message_id": 3225,
            "status": "unseen",
            "created_at": "2018-05-30 17:11:29",
            "updated_at": "2018-05-30 17:11:29",
            "type": null,
            "message": {
                "id": 3225,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       88 to 91 .<br>Thankyou",
                "created_at": "2018-05-30 17:11:29",
                "updated_at": "2018-05-30 17:11:29",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5116,
            "user_id": 989,
            "message_id": 3256,
            "status": "unseen",
            "created_at": "2018-05-30 17:12:23",
            "updated_at": "2018-05-30 17:12:23",
            "type": null,
            "message": {
                "id": 3256,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       91 to 94 .<br>Thankyou",
                "created_at": "2018-05-30 17:12:23",
                "updated_at": "2018-05-30 17:12:23",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5147,
            "user_id": 989,
            "message_id": 3287,
            "status": "unseen",
            "created_at": "2018-05-30 17:12:45",
            "updated_at": "2018-05-30 17:12:45",
            "type": null,
            "message": {
                "id": 3287,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       94 to 97 .<br>Thankyou",
                "created_at": "2018-05-30 17:12:45",
                "updated_at": "2018-05-30 17:12:45",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5178,
            "user_id": 989,
            "message_id": 3318,
            "status": "unseen",
            "created_at": "2018-05-30 17:13:06",
            "updated_at": "2018-05-30 17:13:06",
            "type": null,
            "message": {
                "id": 3318,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       97 to 100 .<br>Thankyou",
                "created_at": "2018-05-30 17:13:06",
                "updated_at": "2018-05-30 17:13:06",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5209,
            "user_id": 989,
            "message_id": 3349,
            "status": "unseen",
            "created_at": "2018-05-30 17:13:55",
            "updated_at": "2018-05-30 17:13:55",
            "type": null,
            "message": {
                "id": 3349,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       100 to 103 .<br>Thankyou",
                "created_at": "2018-05-30 17:13:55",
                "updated_at": "2018-05-30 17:13:55",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5240,
            "user_id": 989,
            "message_id": 3380,
            "status": "unseen",
            "created_at": "2018-05-30 17:14:13",
            "updated_at": "2018-05-30 17:14:13",
            "type": null,
            "message": {
                "id": 3380,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       103 to 106 .<br>Thankyou",
                "created_at": "2018-05-30 17:14:13",
                "updated_at": "2018-05-30 17:14:13",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5271,
            "user_id": 989,
            "message_id": 3411,
            "status": "unseen",
            "created_at": "2018-05-30 17:14:15",
            "updated_at": "2018-05-30 17:14:15",
            "type": null,
            "message": {
                "id": 3411,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       106 to 109 .<br>Thankyou",
                "created_at": "2018-05-30 17:14:15",
                "updated_at": "2018-05-30 17:14:15",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5302,
            "user_id": 989,
            "message_id": 3442,
            "status": "unseen",
            "created_at": "2018-05-30 17:14:17",
            "updated_at": "2018-05-30 17:14:17",
            "type": null,
            "message": {
                "id": 3442,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       109 to 112 .<br>Thankyou",
                "created_at": "2018-05-30 17:14:17",
                "updated_at": "2018-05-30 17:14:17",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5333,
            "user_id": 989,
            "message_id": 3473,
            "status": "unseen",
            "created_at": "2018-05-30 17:14:53",
            "updated_at": "2018-05-30 17:14:53",
            "type": null,
            "message": {
                "id": 3473,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       112 to 114 .<br>Thankyou",
                "created_at": "2018-05-30 17:14:53",
                "updated_at": "2018-05-30 17:14:53",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5364,
            "user_id": 989,
            "message_id": 3504,
            "status": "unseen",
            "created_at": "2018-05-30 17:15:11",
            "updated_at": "2018-05-30 17:15:11",
            "type": null,
            "message": {
                "id": 3504,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       114 to 116 .<br>Thankyou",
                "created_at": "2018-05-30 17:15:11",
                "updated_at": "2018-05-30 17:15:11",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5395,
            "user_id": 989,
            "message_id": 3535,
            "status": "unseen",
            "created_at": "2018-05-30 17:16:11",
            "updated_at": "2018-05-30 17:16:11",
            "type": null,
            "message": {
                "id": 3535,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       116 to 118 .<br>Thankyou",
                "created_at": "2018-05-30 17:16:11",
                "updated_at": "2018-05-30 17:16:11",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5426,
            "user_id": 989,
            "message_id": 3566,
            "status": "unseen",
            "created_at": "2018-05-30 17:16:25",
            "updated_at": "2018-05-30 17:16:25",
            "type": null,
            "message": {
                "id": 3566,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       118 to 120 .<br>Thankyou",
                "created_at": "2018-05-30 17:16:25",
                "updated_at": "2018-05-30 17:16:25",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5457,
            "user_id": 989,
            "message_id": 3597,
            "status": "unseen",
            "created_at": "2018-05-30 17:17:22",
            "updated_at": "2018-05-30 17:17:22",
            "type": null,
            "message": {
                "id": 3597,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       120 to 122 .<br>Thankyou",
                "created_at": "2018-05-30 17:17:22",
                "updated_at": "2018-05-30 17:17:22",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5488,
            "user_id": 989,
            "message_id": 3628,
            "status": "unseen",
            "created_at": "2018-05-30 17:27:29",
            "updated_at": "2018-05-30 17:27:29",
            "type": null,
            "message": {
                "id": 3628,
                "subject": "Change in Product Quantity",
                "message": "Dear BiglyShipper,<br>There is a major Information for you. Just Now, Supplier has changed Quantity of General Knowledge 2019 . Now the Quantity of <b>'General Knowledge 2019 '</b> is changed from       122 to 124 .<br>Thankyou",
                "created_at": "2018-05-30 17:27:29",
                "updated_at": "2018-05-30 17:27:29",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5489,
            "user_id": 989,
            "message_id": 3629,
            "status": "unseen",
            "created_at": "2018-05-31 10:54:24",
            "updated_at": "2018-05-31 10:54:24",
            "type": null,
            "message": {
                "id": 3629,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 10:54:24",
                "updated_at": "2018-05-31 10:54:24",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5490,
            "user_id": 989,
            "message_id": 3630,
            "status": "unseen",
            "created_at": "2018-05-31 10:55:24",
            "updated_at": "2018-05-31 10:55:24",
            "type": null,
            "message": {
                "id": 3630,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 10:55:24",
                "updated_at": "2018-05-31 10:55:24",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5491,
            "user_id": 989,
            "message_id": 3631,
            "status": "unseen",
            "created_at": "2018-05-31 11:15:25",
            "updated_at": "2018-05-31 11:15:25",
            "type": null,
            "message": {
                "id": 3631,
                "subject": "Your Order has been' . shipped ",
                "message": "",
                "created_at": "2018-05-31 11:15:25",
                "updated_at": "2018-05-31 11:15:25",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5492,
            "user_id": 989,
            "message_id": 3632,
            "status": "unseen",
            "created_at": "2018-05-31 11:15:33",
            "updated_at": "2018-05-31 11:15:33",
            "type": null,
            "message": {
                "id": 3632,
                "subject": "Your Order has been' . delivered ",
                "message": "",
                "created_at": "2018-05-31 11:15:33",
                "updated_at": "2018-05-31 11:15:33",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5493,
            "user_id": 989,
            "message_id": 3633,
            "status": "unseen",
            "created_at": "2018-05-31 11:16:46",
            "updated_at": "2018-05-31 11:16:46",
            "type": null,
            "message": {
                "id": 3633,
                "subject": "Your Order has beenshipped",
                "message": "",
                "created_at": "2018-05-31 11:16:46",
                "updated_at": "2018-05-31 11:16:46",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5494,
            "user_id": 989,
            "message_id": 3634,
            "status": "unseen",
            "created_at": "2018-05-31 11:17:14",
            "updated_at": "2018-05-31 11:17:14",
            "type": null,
            "message": {
                "id": 3634,
                "subject": "Your Order has been delivered",
                "message": "",
                "created_at": "2018-05-31 11:17:14",
                "updated_at": "2018-05-31 11:17:14",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5495,
            "user_id": 989,
            "message_id": 3635,
            "status": "unseen",
            "created_at": "2018-05-31 13:00:33",
            "updated_at": "2018-05-31 13:00:33",
            "type": null,
            "message": {
                "id": 3635,
                "subject": "Your Order has been shipped",
                "message": "",
                "created_at": "2018-05-31 13:00:33",
                "updated_at": "2018-05-31 13:00:33",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5496,
            "user_id": 989,
            "message_id": 3636,
            "status": "unseen",
            "created_at": "2018-05-31 13:00:51",
            "updated_at": "2018-05-31 13:00:51",
            "type": null,
            "message": {
                "id": 3636,
                "subject": "Your Order has been delivered",
                "message": "",
                "created_at": "2018-05-31 13:00:51",
                "updated_at": "2018-05-31 13:00:51",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5497,
            "user_id": 989,
            "message_id": 3637,
            "status": "unseen",
            "created_at": "2018-05-31 13:01:21",
            "updated_at": "2018-05-31 13:01:21",
            "type": null,
            "message": {
                "id": 3637,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:01:21",
                "updated_at": "2018-05-31 13:01:21",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5498,
            "user_id": 989,
            "message_id": 3638,
            "status": "unseen",
            "created_at": "2018-05-31 13:05:14",
            "updated_at": "2018-05-31 13:05:14",
            "type": null,
            "message": {
                "id": 3638,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:05:14",
                "updated_at": "2018-05-31 13:05:14",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5499,
            "user_id": 989,
            "message_id": 3639,
            "status": "unseen",
            "created_at": "2018-05-31 13:05:30",
            "updated_at": "2018-05-31 13:05:30",
            "type": null,
            "message": {
                "id": 3639,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:05:30",
                "updated_at": "2018-05-31 13:05:30",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5500,
            "user_id": 989,
            "message_id": 3640,
            "status": "unseen",
            "created_at": "2018-05-31 13:05:46",
            "updated_at": "2018-05-31 13:05:46",
            "type": null,
            "message": {
                "id": 3640,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:05:46",
                "updated_at": "2018-05-31 13:05:46",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5501,
            "user_id": 989,
            "message_id": 3641,
            "status": "unseen",
            "created_at": "2018-05-31 13:05:56",
            "updated_at": "2018-05-31 13:05:56",
            "type": null,
            "message": {
                "id": 3641,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:05:56",
                "updated_at": "2018-05-31 13:05:56",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5502,
            "user_id": 989,
            "message_id": 3642,
            "status": "unseen",
            "created_at": "2018-05-31 13:06:04",
            "updated_at": "2018-05-31 13:06:04",
            "type": null,
            "message": {
                "id": 3642,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:06:04",
                "updated_at": "2018-05-31 13:06:04",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5503,
            "user_id": 989,
            "message_id": 3643,
            "status": "unseen",
            "created_at": "2018-05-31 13:06:25",
            "updated_at": "2018-05-31 13:06:25",
            "type": null,
            "message": {
                "id": 3643,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:06:25",
                "updated_at": "2018-05-31 13:06:25",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5504,
            "user_id": 989,
            "message_id": 3644,
            "status": "unseen",
            "created_at": "2018-05-31 13:06:41",
            "updated_at": "2018-05-31 13:06:41",
            "type": null,
            "message": {
                "id": 3644,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:06:41",
                "updated_at": "2018-05-31 13:06:41",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5505,
            "user_id": 989,
            "message_id": 3645,
            "status": "unseen",
            "created_at": "2018-05-31 13:06:57",
            "updated_at": "2018-05-31 13:06:57",
            "type": null,
            "message": {
                "id": 3645,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:06:57",
                "updated_at": "2018-05-31 13:06:57",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5506,
            "user_id": 989,
            "message_id": 3646,
            "status": "unseen",
            "created_at": "2018-05-31 13:07:41",
            "updated_at": "2018-05-31 13:07:41",
            "type": null,
            "message": {
                "id": 3646,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:07:41",
                "updated_at": "2018-05-31 13:07:41",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5507,
            "user_id": 989,
            "message_id": 3647,
            "status": "unseen",
            "created_at": "2018-05-31 13:07:48",
            "updated_at": "2018-05-31 13:07:48",
            "type": null,
            "message": {
                "id": 3647,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:07:48",
                "updated_at": "2018-05-31 13:07:48",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5508,
            "user_id": 989,
            "message_id": 3648,
            "status": "unseen",
            "created_at": "2018-05-31 13:08:15",
            "updated_at": "2018-05-31 13:08:15",
            "type": null,
            "message": {
                "id": 3648,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:08:15",
                "updated_at": "2018-05-31 13:08:15",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5509,
            "user_id": 989,
            "message_id": 3649,
            "status": "unseen",
            "created_at": "2018-05-31 13:10:04",
            "updated_at": "2018-05-31 13:10:04",
            "type": null,
            "message": {
                "id": 3649,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:10:04",
                "updated_at": "2018-05-31 13:10:04",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5510,
            "user_id": 989,
            "message_id": 3650,
            "status": "unseen",
            "created_at": "2018-05-31 13:10:24",
            "updated_at": "2018-05-31 13:10:24",
            "type": null,
            "message": {
                "id": 3650,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:10:24",
                "updated_at": "2018-05-31 13:10:24",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5511,
            "user_id": 989,
            "message_id": 3651,
            "status": "unseen",
            "created_at": "2018-05-31 13:12:14",
            "updated_at": "2018-05-31 13:12:14",
            "type": null,
            "message": {
                "id": 3651,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 13:12:14",
                "updated_at": "2018-05-31 13:12:14",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5512,
            "user_id": 989,
            "message_id": 3652,
            "status": "unseen",
            "created_at": "2018-05-31 14:10:25",
            "updated_at": "2018-05-31 14:10:25",
            "type": null,
            "message": {
                "id": 3652,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 14:10:25",
                "updated_at": "2018-05-31 14:10:25",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5513,
            "user_id": 989,
            "message_id": 3653,
            "status": "unseen",
            "created_at": "2018-05-31 14:11:07",
            "updated_at": "2018-05-31 14:11:07",
            "type": null,
            "message": {
                "id": 3653,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 14:11:07",
                "updated_at": "2018-05-31 14:11:07",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5514,
            "user_id": 989,
            "message_id": 3654,
            "status": "unseen",
            "created_at": "2018-05-31 15:05:34",
            "updated_at": "2018-05-31 15:05:34",
            "type": null,
            "message": {
                "id": 3654,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 15:05:34",
                "updated_at": "2018-05-31 15:05:34",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5515,
            "user_id": 989,
            "message_id": 3655,
            "status": "unseen",
            "created_at": "2018-05-31 15:07:56",
            "updated_at": "2018-05-31 15:07:56",
            "type": null,
            "message": {
                "id": 3655,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 15:07:56",
                "updated_at": "2018-05-31 15:07:56",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        },
        {
            "id": 5516,
            "user_id": 989,
            "message_id": 3656,
            "status": "unseen",
            "created_at": "2018-05-31 15:08:21",
            "updated_at": "2018-05-31 15:08:21",
            "type": null,
            "message": {
                "id": 3656,
                "subject": "Congratulations !! Notification Done",
                "message": "",
                "created_at": "2018-05-31 15:08:21",
                "updated_at": "2018-05-31 15:08:21",
                "expires_at": "0000-00-00 00:00:00",
                "type": ""
            }
        }
    ]
}
```

<!-- 33 -->

##  Check Profile Api (Get)

**API** `http://localhost:8000/api/user/check`

**Method** : GET

### Response :

_Example_

```
{
    "user_detail": 1,
    "billing_address": 1,
    "shipping_address": 0,
    "bank_details": 1
}

```

<!-- 34 -->


##  View Bank Details of user

**API** `http://localhost:8000/api/bank/details`

**Method** : GET

### Response :

_Example_

```
{
    "bank": {
        "id": 121,
        "user_id": 989,
        "organization_id": 951,
        "bank_name": "nkanikefwa",
        "account_number": "27974374979479",
        "account_holder_name": "sakshi",
        "IFSC_code": "UZXNDJD"
    },
    "responseCode": 200,
    "responseMessage": "Bank Details Found"
}
```



<!-- 35 -->


##  Insert or Update Bank Details

**API** `http://localhost:8000/api/bank/details`

**Method** : Post

### Request :

_Example_

```
{
    "bank_name" : "nkanikefwa",
    "account_number" : 27974374979479,
    "account_holder_name" : "sakshi",
    "IFSC_code" : "UZXNDJD" 
}
```


### Response
```
{
    "bank": {
        "id": 121,
        "user_id": 989,
        "organization_id": 951,
        "bank_name": "nkanikefwa",
        "account_number": "27974374979479",
        "account_holder_name": "sakshi",
        "IFSC_code": "UZXNDJD"
    },
    "responseCode": 200,
    "responseMessage": "Bank Details Found"
}
```




