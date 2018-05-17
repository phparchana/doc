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
    23 . Order Details
    24. Get Cancel Reasons
    25. Cancel Order








##  Register (POST)

**API** `http://localhost:8000/api/register`

**Method** : POST

### Request :

_Example_

```


  {
    "name": "user name",
    "email" : "name@email.com",
    "fb_id" : 231
}

```


### Response :


_Example_

```

{
   "name": "user name",
   "email": "name@email.com",
   "updated_at": "2018-04-04 12:29:36",
   "created_at": "2018-04-04 12:29:36",
   "id": 532
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
                "id": 1,
                "user_id": 1,
                "name": "cfdsgvd",
                "slug": "",
                "bdpin": "1b2327d1-313d-368b-bd91-0638931d5ff5",
                "brand_id": null,
                "model": null,
                "sku": "6b9390ec-1992-3bcb-b658-5743a401ca9c",
                "description": "There was a long tail, certainly,' said Alice, swallowing down her anger as well as if nothing had happened. 'How am I then? Tell me that first, and then, and holding it to be found: all she could.",
                "specification": null,
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
                "isWishlist": 1,
                "organization": null,
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
                "id": 2,
                "user_id": 2,
                "name": "Wunsch, Kerluke and Kuphal",
                "slug": "",
                "bdpin": "4c9d0997-baed-3284-827c-a0aa81b51bfb",
                "brand_id": null,
                "model": null,
                "sku": "26463d4a-d488-35b8-b61f-84d865a1e943",
                "description": "Alice, in a tone of the door that led into the court, by the hedge!' then silence, and then the puppy began a series of short charges at the March Hare said in an agony of terror. 'Oh, there goes.",
                "specification": null,
                "weight": "1648.00",
                "length": "1464.00",
                "width": "4143.00",
                "height": "4618.00",
                "amount": "68.00",
                "quantity": 16,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-03-01 10:54:50",
                "updated_at": "2018-03-01 10:54:50",
                "min_price": "0.00",
                "max_price": "0.00",
                "shipping_charge": "0.00",
                "attributes": [],
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 3,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/technics/3",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/technics/3",
                        "large": "http://lorempixel.com/1280/720/technics/3",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 23,
                        "name": "Ledner-Harber",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 32,
                        "name": "Denesik Group",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 27,
                        "name": "Emmerich-Schultz",
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
                "id": 3,
                "user_id": 1,
                "name": "Rogahn-Corkery",
                "slug": "",
                "bdpin": "875a9c56-0d9b-3215-ac5f-8ea83e05b9c4",
                "brand_id": null,
                "model": null,
                "sku": "90e353ca-5fca-3df5-8989-6bed37d9368b",
                "description": "Mock Turtle repeated thoughtfully. 'I should like to be managed? I suppose Dinah'll be sending me on messages next!' And she began again: 'Ou est ma chatte?' which was immediately suppressed by the.",
                "specification": null,
                "weight": "3700.00",
                "length": "2745.00",
                "width": "3881.00",
                "height": "744.00",
                "amount": "18.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 4,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/business/4",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/business/4",
                        "large": "http://lorempixel.com/1280/720/business/4",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 5,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/sports/4",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/sports/4",
                        "large": "http://lorempixel.com/1280/720/sports/4",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 47,
                        "name": "Ferry-Larkin",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 46,
                        "name": "Schowalter, Yost and Fisher",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 33,
                        "name": "Glover Group",
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
                "id": 4,
                "user_id": 1,
                "name": "McClure-Jakubowski",
                "slug": "",
                "bdpin": "98ca4aa1-2555-3ec0-9918-89eb0e980c38",
                "brand_id": null,
                "model": null,
                "sku": "0d4471c9-5683-3f2c-8717-8c24152dde61",
                "description": "Mock Turtle said: 'no wise fish would go through,' thought poor Alice, 'to speak to this last remark that had fluttered down from the time at the end.' 'If you didn't sign it,' said Alice. 'That's.",
                "specification": null,
                "weight": "7469.00",
                "length": "4855.00",
                "width": "7561.00",
                "height": "1356.00",
                "amount": "91.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 6,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/technics/5",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/technics/5",
                        "large": "http://lorempixel.com/1280/720/technics/5",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 7,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/transport/5",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/transport/5",
                        "large": "http://lorempixel.com/1280/720/transport/5",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 8,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/business/5",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/business/5",
                        "large": "http://lorempixel.com/1280/720/business/5",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 9,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nightlife/5",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nightlife/5",
                        "large": "http://lorempixel.com/1280/720/nightlife/5",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 10,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/food/5",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/food/5",
                        "large": "http://lorempixel.com/1280/720/food/5",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 39,
                        "name": "Gutmann-McCullough",
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
                "id": 5,
                "user_id": 1,
                "name": "Dare-Ullrich",
                "slug": "",
                "bdpin": "97be2e6f-77bc-3ac9-829d-e36d82dc9738",
                "brand_id": null,
                "model": null,
                "sku": "a3081055-0a52-349b-aa00-4cf9cb2d7c34",
                "description": "ALL RETURNED FROM HIM TO YOU,\"' said Alice. 'Then you should say what you were or might have been a RED rose-tree, and we won't talk about cats or dogs either, if you like,' said the Rabbit's voice;.",
                "specification": null,
                "weight": "3578.00",
                "length": "593.00",
                "width": "8598.00",
                "height": "9802.00",
                "amount": "83.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 11,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/people/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/people/6",
                        "large": "http://lorempixel.com/1280/720/people/6",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 12,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nightlife/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nightlife/6",
                        "large": "http://lorempixel.com/1280/720/nightlife/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 13,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/people/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/people/6",
                        "large": "http://lorempixel.com/1280/720/people/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 14,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nature/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nature/6",
                        "large": "http://lorempixel.com/1280/720/nature/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 15,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/people/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/people/6",
                        "large": "http://lorempixel.com/1280/720/people/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 16,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nightlife/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nightlife/6",
                        "large": "http://lorempixel.com/1280/720/nightlife/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 17,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nature/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nature/6",
                        "large": "http://lorempixel.com/1280/720/nature/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 47,
                        "name": "Ferry-Larkin",
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
                "id": 6,
                "user_id": 1,
                "name": "Becker Inc",
                "slug": "",
                "bdpin": "8b6b5866-bc7b-3ab5-8bd9-5790e2295379",
                "brand_id": null,
                "model": null,
                "sku": "9a739e95-43f0-3349-8e72-818a27ac592e",
                "description": "King, 'that saves a world of trouble, you know, this sort of knot, and then the different branches of Arithmetic--Ambition, Distraction, Uglification, and Derision.' 'I never was so large a house.",
                "specification": null,
                "weight": "8032.00",
                "length": "4533.00",
                "width": "1614.00",
                "height": "687.00",
                "amount": "92.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 18,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/business/7",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/business/7",
                        "large": "http://lorempixel.com/1280/720/business/7",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 19,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/people/7",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/people/7",
                        "large": "http://lorempixel.com/1280/720/people/7",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 20,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nature/7",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nature/7",
                        "large": "http://lorempixel.com/1280/720/nature/7",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 21,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/sports/7",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/sports/7",
                        "large": "http://lorempixel.com/1280/720/sports/7",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 22,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/fashion/7",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/fashion/7",
                        "large": "http://lorempixel.com/1280/720/fashion/7",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 23,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/business/7",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/business/7",
                        "large": "http://lorempixel.com/1280/720/business/7",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 24,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/transport/7",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/transport/7",
                        "large": "http://lorempixel.com/1280/720/transport/7",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 25,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/transport/7",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/transport/7",
                        "large": "http://lorempixel.com/1280/720/transport/7",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 11,
                        "name": "Stracke PLC",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 5,
                        "name": "Jacobi-Jakubowski",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 44,
                        "name": "Wunsch Inc",
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
                "id": 7,
                "user_id": 1,
                "name": "Fahey Group",
                "slug": "",
                "bdpin": "4f7756c2-d481-3dda-92f6-baf9d6cc624b",
                "brand_id": null,
                "model": null,
                "sku": "7f00dd58-74b0-30b5-a637-3be164e3ee5c",
                "description": "There was nothing on it except a little girl,' said Alice, rather doubtfully, as she went round the thistle again; then the Rabbit's voice along--'Catch him, you by the White Rabbit put on your.",
                "specification": null,
                "weight": "7591.00",
                "length": "8825.00",
                "width": "5296.00",
                "height": "8837.00",
                "amount": "64.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 26,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nightlife/8",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nightlife/8",
                        "large": "http://lorempixel.com/1280/720/nightlife/8",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 27,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/food/8",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/food/8",
                        "large": "http://lorempixel.com/1280/720/food/8",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 28,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/business/8",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/business/8",
                        "large": "http://lorempixel.com/1280/720/business/8",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 29,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nightlife/8",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nightlife/8",
                        "large": "http://lorempixel.com/1280/720/nightlife/8",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 30,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/fashion/8",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/fashion/8",
                        "large": "http://lorempixel.com/1280/720/fashion/8",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 31,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/technics/8",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/technics/8",
                        "large": "http://lorempixel.com/1280/720/technics/8",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 32,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/business/8",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/business/8",
                        "large": "http://lorempixel.com/1280/720/business/8",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 45,
                        "name": "Wunsch-Waters",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 35,
                        "name": "Hackett PLC",
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
                "id": 8,
                "user_id": 1,
                "name": "Effertz-Rau",
                "slug": "",
                "bdpin": "e12465f2-e9e4-3ab3-b40c-5869e8a83fce",
                "brand_id": null,
                "model": null,
                "sku": "58f582a2-01da-34df-826f-61d078ffceb6",
                "description": "And she began thinking over other children she knew, who might do very well as she spoke; 'either you or your head must be removed,' said the Queen, pointing to the jury, in a tone of great.",
                "specification": null,
                "weight": "7247.00",
                "length": "4806.00",
                "width": "1258.00",
                "height": "4889.00",
                "amount": "22.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 33,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/transport/9",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/transport/9",
                        "large": "http://lorempixel.com/1280/720/transport/9",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 34,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nightlife/9",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nightlife/9",
                        "large": "http://lorempixel.com/1280/720/nightlife/9",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 35,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/food/9",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/food/9",
                        "large": "http://lorempixel.com/1280/720/food/9",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 36,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/people/9",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/people/9",
                        "large": "http://lorempixel.com/1280/720/people/9",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 47,
                        "name": "Ferry-Larkin",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 12,
                        "name": "Johnston-Kuhn",
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
                "id": 9,
                "user_id": 1,
                "name": "Zulauf PLC",
                "slug": "",
                "bdpin": "252f5236-0aae-3409-8624-8b669e2cb925",
                "brand_id": null,
                "model": null,
                "sku": "8352b0b3-c323-3115-a284-7f03a81b124e",
                "description": "She pitied him deeply. 'What is his sorrow?' she asked the Mock Turtle yet?' 'No,' said Alice. 'Then it wasn't very civil of you to set them free, Exactly as we needn't try to find my way into that.",
                "specification": null,
                "weight": "5335.00",
                "length": "417.00",
                "width": "7665.00",
                "height": "995.00",
                "amount": "81.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 37,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/technics/10",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/technics/10",
                        "large": "http://lorempixel.com/1280/720/technics/10",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 38,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/technics/10",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/technics/10",
                        "large": "http://lorempixel.com/1280/720/technics/10",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 3,
                        "name": "Kautzer-Goyette",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 6,
                        "name": "Maggio Ltd",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 45,
                        "name": "Wunsch-Waters",
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
                "id": 10,
                "user_id": 1,
                "name": "Stamm, Jones and Buckridge",
                "slug": "",
                "bdpin": "42f0495c-7b89-3aa9-9221-509eb83f9ac5",
                "brand_id": null,
                "model": null,
                "sku": "93bc3aa3-dac9-349c-ae13-10a89ed51fb7",
                "description": "Alice went on, taking first one side and up I goes like a telescope! I think that proved it at last, more calmly, though still sobbing a little bit of mushroom, and raised herself to about two feet.",
                "specification": null,
                "weight": "3471.00",
                "length": "2333.00",
                "width": "3312.00",
                "height": "1658.00",
                "amount": "63.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 39,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/business/1",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/business/1",
                        "large": "http://lorempixel.com/1280/720/business/1",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 40,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/technics/1",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/technics/1",
                        "large": "http://lorempixel.com/1280/720/technics/1",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 41,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/transport/1",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/transport/1",
                        "large": "http://lorempixel.com/1280/720/transport/1",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 1,
                        "name": "Torphy-Schimmel",
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
                "specification": null,
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
                "isWishlist": 1,
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
                "id": 12,
                "user_id": 1,
                "name": "O'Reilly LLC",
                "slug": "",
                "bdpin": "2413bc07-e121-32b8-a3d1-103b7bd3108d",
                "brand_id": null,
                "model": null,
                "sku": "0e10efef-13e6-3377-9507-20efa9042f0f",
                "description": "products seem good",
                "specification": null,
                "weight": "6917.00",
                "length": "1592.00",
                "width": "629.00",
                "height": "8460.00",
                "amount": "18.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 45,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/sports/3",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/sports/3",
                        "large": "http://lorempixel.com/1280/720/sports/3",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 46,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nature/3",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nature/3",
                        "large": "http://lorempixel.com/1280/720/nature/3",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 47,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/food/3",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/food/3",
                        "large": "http://lorempixel.com/1280/720/food/3",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 20,
                        "name": "Carroll-Runolfsdottir",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 36,
                        "name": "Hegmann Ltd",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 22,
                        "name": "Thiel Group",
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
                "id": 13,
                "user_id": 1,
                "name": "Bergnaum Group",
                "slug": "",
                "bdpin": "5e979a98-bd51-3aaf-a4a2-5f61159e2831",
                "brand_id": null,
                "model": null,
                "sku": "4396f31f-4e58-3242-96f9-27b520e03e4b",
                "description": "Queen will hear you! You see, she came in with a kind of serpent, that's all the jurymen on to her very much what would be a person of authority among them, called out, 'Sit down, all of them bowed.",
                "specification": null,
                "weight": "7502.00",
                "length": "8119.00",
                "width": "165.00",
                "height": "158.00",
                "amount": "56.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 48,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/technics/4",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/technics/4",
                        "large": "http://lorempixel.com/1280/720/technics/4",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 33,
                        "name": "Glover Group",
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
                "id": 14,
                "user_id": 1,
                "name": "Langosh Group",
                "slug": "",
                "bdpin": "17b2501b-fc87-3522-ab9a-e5f606b66664",
                "brand_id": null,
                "model": null,
                "sku": "8ed17792-39e6-34bf-883d-d0e13747d3fc",
                "description": "I THINK,' said Alice. 'Call it what you mean,' the March Hare, who had been jumping about like mad things all this grand procession, came THE KING AND QUEEN OF HEARTS. Alice was silent. The King.",
                "specification": null,
                "weight": "3281.00",
                "length": "2642.00",
                "width": "9059.00",
                "height": "622.00",
                "amount": "100.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 49,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nature/5",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nature/5",
                        "large": "http://lorempixel.com/1280/720/nature/5",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 50,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/people/5",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/people/5",
                        "large": "http://lorempixel.com/1280/720/people/5",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 1,
                        "name": "Torphy-Schimmel",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 14,
                        "name": "Koepp and Sons",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    },
                    {
                        "id": 36,
                        "name": "Hegmann Ltd",
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
                "id": 15,
                "user_id": 1,
                "name": "Volkman, Mayer and Wuckert",
                "slug": "",
                "bdpin": "f0291e04-e26d-3bed-88d8-88344dd7a50e",
                "brand_id": null,
                "model": null,
                "sku": "04dfddd7-a58b-3834-b6eb-04542379d258",
                "description": "I don't know what you like,' said the King triumphantly, pointing to the Dormouse, who was peeping anxiously into its nest. Alice crouched down among the distant sobs of the bread-and-butter. Just.",
                "specification": null,
                "weight": "4564.00",
                "length": "449.00",
                "width": "4229.00",
                "height": "6349.00",
                "amount": "95.00",
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
                "isWishlist": 0,
                "organization": null,
                "media": [
                    {
                        "id": 51,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nightlife/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nightlife/6",
                        "large": "http://lorempixel.com/1280/720/nightlife/6",
                        "caption": null,
                        "default": 1,
                        "check": "pending"
                    },
                    {
                        "id": 52,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nightlife/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nightlife/6",
                        "large": "http://lorempixel.com/1280/720/nightlife/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 53,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/people/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/people/6",
                        "large": "http://lorempixel.com/1280/720/people/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 54,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/business/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/business/6",
                        "large": "http://lorempixel.com/1280/720/business/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 55,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/transport/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/transport/6",
                        "large": "http://lorempixel.com/1280/720/transport/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 56,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/people/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/people/6",
                        "large": "http://lorempixel.com/1280/720/people/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 57,
                        "mime": "",
                        "thumb": "http://lorempixel.com/270/220/nature/6",
                        "small": null,
                        "medium": "http://lorempixel.com/480/360/nature/6",
                        "large": "http://lorempixel.com/1280/720/nature/6",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 11,
                        "name": "Stracke PLC",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ]
            }
        ],
        "from": 1,
        "last_page": 67,
        "next_page_url": "http://localhost:8000/api/products?page=2",
        "path": "http://localhost:8000/api/products",
        "per_page": 15,
        "prev_page_url": null,
        "to": 15,
        "total": 1003
    },
    "filter": {
        "categories": [
            {
                "id": 26,
                "name": "Auer-Doyle"
            },
            {
                "id": 51,
                "name": "bag"
            },
            {
                "id": 20,
                "name": "Carroll-Runolfsdottir"
            },
            {
                "id": 19,
                "name": "Carroll-Swaniawski"
            },
            {
                "id": 25,
                "name": "Deckow Ltd"
            },
            {
                "id": 32,
                "name": "Denesik Group"
            },
            {
                "id": 17,
                "name": "Denesik-Ondricka"
            },
            {
                "id": 24,
                "name": "Dicki-Wilkinson"
            },
            {
                "id": 27,
                "name": "Emmerich-Schultz"
            },
            {
                "id": 37,
                "name": "Fahey Group"
            },
            {
                "id": 47,
                "name": "Ferry-Larkin"
            },
            {
                "id": 21,
                "name": "Gerlach, Ward and Grimes"
            },
            {
                "id": 33,
                "name": "Glover Group"
            },
            {
                "id": 39,
                "name": "Gutmann-McCullough"
            },
            {
                "id": 35,
                "name": "Hackett PLC"
            },
            {
                "id": 36,
                "name": "Hegmann Ltd"
            },
            {
                "id": 31,
                "name": "Hyatt, Maggio and Russel"
            },
            {
                "id": 5,
                "name": "Jacobi-Jakubowski"
            },
            {
                "id": 12,
                "name": "Johnston-Kuhn"
            },
            {
                "id": 3,
                "name": "Kautzer-Goyette"
            },
            {
                "id": 38,
                "name": "Keebler-Huels"
            },
            {
                "id": 14,
                "name": "Koepp and Sons"
            },
            {
                "id": 7,
                "name": "Langosh, Jast and Ferry"
            },
            {
                "id": 23,
                "name": "Ledner-Harber"
            },
            {
                "id": 28,
                "name": "Lubowitz Group"
            },
            {
                "id": 15,
                "name": "Lubowitz, Borer and Harvey"
            },
            {
                "id": 34,
                "name": "Lynch, Jast and Osinski"
            },
            {
                "id": 16,
                "name": "Macejkovic-Bradtke"
            },
            {
                "id": 6,
                "name": "Maggio Ltd"
            },
            {
                "id": 4,
                "name": "Marquardt-Gleichner"
            },
            {
                "id": 49,
                "name": "Mills-Kihn"
            },
            {
                "id": 13,
                "name": "Nienow, McClure and Kris"
            },
            {
                "id": 10,
                "name": "Ondricka, Sanford and Frami"
            },
            {
                "id": 43,
                "name": "Reichert PLC"
            },
            {
                "id": 8,
                "name": "Rice PLC"
            },
            {
                "id": 2,
                "name": "Rodriguez, Moore and Balistreri"
            },
            {
                "id": 46,
                "name": "Schowalter, Yost and Fisher"
            },
            {
                "id": 29,
                "name": "Senger and Sons"
            },
            {
                "id": 50,
                "name": "Simonis PLC"
            },
            {
                "id": 42,
                "name": "Spencer Group"
            },
            {
                "id": 11,
                "name": "Stracke PLC"
            },
            {
                "id": 40,
                "name": "Stracke, Fadel and Rau"
            },
            {
                "id": 22,
                "name": "Thiel Group"
            },
            {
                "id": 1,
                "name": "Torphy-Schimmel"
            },
            {
                "id": 48,
                "name": "Tremblay-Pollich"
            },
            {
                "id": 41,
                "name": "West Inc"
            },
            {
                "id": 9,
                "name": "White, Boyer and Kuhlman"
            },
            {
                "id": 18,
                "name": "Wiza-Doyle"
            },
            {
                "id": 44,
                "name": "Wunsch Inc"
            },
            {
                "id": 45,
                "name": "Wunsch-Waters"
            },
            {
                "id": 30,
                "name": "Zieme, McClure and Kling"
            }
        ],
        "suppliers": [
            {
                "id": 2,
                "name": "vendor"
            },
            {
                "id": 22,
                "name": "Miss Shaina Casper"
            },
            {
                "id": 514,
                "name": "test"
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
        "organization": {
            "id": 794,
            "user_id": "830",
            "type_id": "3",
            "name": "Desigrace",
            "logo": "http://s.bigly.io/logo/1524569504-UbCDXlsCWHeWANF.png",
            "gst": "",
            "incorporation_number": "",
            "address": "G-12B, Street no-5 Arjun Nagar, Delhi-51",
            "introduction": "we are Manufacturer and dealer in unisex T-shirts and girls leggings",
            "created_at": "2018-04-24 11:29:45",
            "updated_at": "2018-04-24 11:31:44",
            "city": "Delhi",
            "state": "Delhi",
            "pincode": "110051",
            "country": "India"
        },
        "categories": [
            {
                "id": 62,
                "name": "Women's Clothing",
                "description": "",
                "meta_title": "",
                "meta_des": "",
                "meta_keywords": "",
                "slug": "",
                "parent_id": null,
                "status": "1"
            }
        ],
        "attributes": [
            {
                "id": 5214,
                "value": "Red",
                "quantity": null,
                "price": null,
                "name": "Color",
                "attr_id": "1",
                "children": [
                    {
                        "id": 5215,
                        "value": "28",
                        "quantity": "485",
                        "price": null,
                        "attr_id": "2"
                    },
                    {
                        "id": 5216,
                        "value": "30",
                        "quantity": "486",
                        "price": null,
                        "attr_id": "2"
                    },
                    {
                        "id": 5217,
                        "value": "32",
                        "quantity": "487",
                        "price": null,
                        "attr_id": "2"
                    },
                    {
                        "id": 5218,
                        "value": "34",
                        "quantity": "488",
                        "price": null,
                        "attr_id": "2"
                    },
                    {
                        "id": 5219,
                        "value": "36",
                        "quantity": "489",
                        "price": null,
                        "attr_id": "2"
                    },
                    {
                        "id": 5220,
                        "value": "38",
                        "quantity": "490",
                        "price": null,
                        "attr_id": "2"
                    }
                ]
            }
        ],
        "user": {
            "id": 830,
            "name": "HIMANSHU GARG",
            "username": null,
            "email": "desigrace.gfh@gmail.com",
            "status": "1",
            "phone": "9654716652",
            "created_at": "Apr 24, 2018",
            "updated_at": "2018-04-24 11:29:45",
            "type": "vendor"
        },
        "rating": {
            "rating": "3.00000",
            "entity_id": "22936"
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
        "user_id": 510,
        "product_id": 1011,
        "quantity": 10,
        "payment_mode": "COD",
        "attribute_id": 17,
        "amount": 50,
        "type": "cart",
        "updated_at": "2018-05-07 15:20:47",
        "created_at": "2018-05-07 15:20:47",
        "id": 3
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
    "type" : "shipping"
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


**API** `http://localhost:8000/api/orderDetail/199`

**Method** : Get

### Response :


_Example_

```
{
    "order_detail": {
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
        },
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
        "attribute_data": null,
        "organization": null
    },
    "shipping_address": null,
    "responseMessage": "User All Orders",
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


**API** `http://dropship.bigly.io/api/orderCancel/282`

**Method** : Post

### Request :


_Example_

```
{
    "reason_id" : 2
}

```

### Response

```
