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
                "quantity": 521,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2018-05-02 18:11:59",
                "updated_at": "2018-05-02 18:12:05",
                "min_price": "121.00",
                "max_price": "1200.00",
                "shipping_charge": "2.00",
                "attributes": [
                    {
                        "id": 16,
                        "value": "blue",
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
                                "attr_id": 3
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
        "path": "http://localhost:8000/api/products",
        "per_page": 15,
        "prev_page_url": null,
        "to": 2,
        "total": 2
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
    "quantity": 521,
    "status": 1,
    "source": "bigly",
    "source_id": null,
    "created_at": "2018-05-02 18:11:59",
    "updated_at": "2018-05-02 18:12:05",
    "min_price": "121.00",
    "max_price": "1200.00",
    "shipping_charge": "2.00",
    "brand_name": "dsgesdge",
    "brand": {
        "id": 9,
        "name": "dsgesdge"
    },
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
    "categories": [],
    "attributes": [
        {
            "id": 16,
            "value": "blue",
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
                    "attr_id": 3
                }
            ]
        }
    ],
    "user": {
        "id": 2,
        "name": "vendor",
        "username": null,
        "email": "supplier@gmail.com",
        "status": 1,
        "phone": "1234567890",
        "created_at": "Mar 01, 2018",
        "updated_at": "2018-03-08 10:04:56",
        "type": "vendor"
    },
    "rating": {
        "rating": "4.00000",
        "entity_id": 1011
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
    "wishlist": null
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
            "id": 71,
            "order_id": 187,
            "product_id": 1011,
            "attribute_id": 17,
            "name": "sZEfgfr",
            "quantity": 1,
            "amount": 21,
            "organization_id": 2,
            "status": "completed",
            "shipment_id": "902549187",
            "shipping_charge": "2.00",
            "media": [
                {
                    "id": 298,
                    "mime": "",
                    "thumb": "http://lorempixel.com/270/220/technics/2",
                    "small": null,
                    "medium": "http://lorempixel.com/480/360/technics/2",
                    "large": "http://lorempixel.com/1280/720/technics/2",
                    "caption": null,
                    "default": 1,
                    "check": "pending"
                },
                {
                    "id": 299,
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
                    "id": 300,
                    "mime": "",
                    "thumb": "http://lorempixel.com/270/220/technics/2",
                    "small": null,
                    "medium": "http://lorempixel.com/480/360/technics/2",
                    "large": "http://lorempixel.com/1280/720/technics/2",
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                },
                {
                    "id": 301,
                    "mime": "",
                    "thumb": "http://lorempixel.com/270/220/food/2",
                    "small": null,
                    "medium": "http://lorempixel.com/480/360/food/2",
                    "large": "http://lorempixel.com/1280/720/food/2",
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                },
                {
                    "id": 302,
                    "mime": "",
                    "thumb": "http://lorempixel.com/270/220/sports/2",
                    "small": null,
                    "medium": "http://lorempixel.com/480/360/sports/2",
                    "large": "http://lorempixel.com/1280/720/sports/2",
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                },
                {
                    "id": 303,
                    "mime": "",
                    "thumb": "http://lorempixel.com/270/220/business/2",
                    "small": null,
                    "medium": "http://lorempixel.com/480/360/business/2",
                    "large": "http://lorempixel.com/1280/720/business/2",
                    "caption": null,
                    "default": 0,
                    "check": "pending"
                }
            ],
            "size": {
                "id": 17,
                "value": "50"
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
        "id": 84,
        "order_id": 199,
        "product_id": 1011,
        "attribute_id": 17,
        "name": "sZEfgfr",
        "quantity": 10,
        "amount": 50,
        "organization_id": 0,
        "status": "placed",
        "shipment_id": "",
        "shipping_charge": "2.00",
        "type": null,
        "product": {
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
            "quantity": 521,
            "status": 1,
            "source": "bigly",
            "source_id": null,
            "created_at": "2018-05-02 18:11:59",
            "updated_at": "2018-05-02 18:12:05",
            "min_price": "121.00",
            "max_price": "1200.00",
            "shipping_charge": "2.00",
            "brand_name": "dsgesdge",
            "brand": {
                "id": 9,
                "name": "dsgesdge"
            }
        },
        "media": [
            {
                "id": 364,
                "mime": "",
                "thumb": "http://lorempixel.com/270/220/business/5",
                "small": null,
                "medium": "http://lorempixel.com/480/360/business/5",
                "large": "http://lorempixel.com/1280/720/business/5",
                "caption": null,
                "default": 1,
                "check": "pending"
            },
            {
                "id": 365,
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
                "id": 366,
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
                "id": 367,
                "mime": "",
                "thumb": "http://lorempixel.com/270/220/sports/5",
                "small": null,
                "medium": "http://lorempixel.com/480/360/sports/5",
                "large": "http://lorempixel.com/1280/720/sports/5",
                "caption": null,
                "default": 0,
                "check": "pending"
            },
            {
                "id": 368,
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
                "id": 369,
                "mime": "",
                "thumb": "http://lorempixel.com/270/220/business/5",
                "small": null,
                "medium": "http://lorempixel.com/480/360/business/5",
                "large": "http://lorempixel.com/1280/720/business/5",
                "caption": null,
                "default": 0,
                "check": "pending"
            }
        ],
        "order": {
            "id": 199,
            "user_id": 510,
            "client_id": 0,
            "name": "DS_Order_auJ2cAixf82rYHQm",
            "invoice": "",
            "amount": "21.00",
            "created_at": "2018-05-11 16:05:32",
            "updated_at": "2018-05-11 16:05:32",
            "status": "placed",
            "price": "210.00",
            "payment_method": "COD"
        },
        "organization": null,
        "size": {
            "id": 17,
            "value": "50"
        }
    },
    "cart_address": {
        "id": 2,
        "user_id": 510,
        "order_id": 199,
        "name": "sanjay",
        "email": null,
        "mobile": "1234567890",
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
        "created_at": "2018-04-21 06:21:48",
        "updated_at": "2018-05-11 16:05:32"
    },
    "responseMessage": "User All Orders",
    "responseCode": 200
}
```
