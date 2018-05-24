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








##  Register (POST)

**API** `http://localhost:8000/api/register`

**Method** : POST

### Request :

_Example_

```


{
   "access_token" : "svdch",
   "device_token" : "dbhjdsbdvfj",
   "device_type" : "mobsdfs"
}

```


### Response :


_Example_

```
{
    "accessToken": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6Ijg2NjAxNmU2NzE0MzdiNGM2MTgyZTA5NThjZmQ0MjQ0ODcxMDIzYWJmODQ1NDc1MTYyMjFlNzc3MDMyNTRhZGQzNTViMjQ2MzM4YzEyYjI5In0.eyJhdWQiOiIyNDYiLCJqdGkiOiI4NjYwMTZlNjcxNDM3YjRjNjE4MmUwOTU4Y2ZkNDI0NDg3MTAyM2FiZjg0NTQ3NTE2MjIxZTc3NzAzMjU0YWRkMzU1YjI0NjMzOGMxMmIyOSIsImlhdCI6MTUyNzE1NjQ3OCwibmJmIjoxNTI3MTU2NDc4LCJleHAiOjE1NTg2OTI0NzgsInN1YiI6Ijk4OSIsInNjb3BlcyI6W119.i1TYC6r33x0W-cRAt2bYoFWAAn8oRCft9OiriTnDbTQjHB8y4YRzdhX9ERXvKs8su3aOr-YGLKca8_uSJTbt1WfU4IC45l9DImEh2lexgocjQTXku1MWXE6JHDNaWpqL1FaFBAwkG0uFuRwWopqEuSesT28-EjCHN2PPoLZMhNYOQggziucZG_VJCQkMRFzPvFE9HBRwht9rH1Cftnx9ziwl2d1uRZo_6CdJ4HWBba6jyv6NQK9ycHgtUV_Votq5BBe8hYqVYv38f9OKP-FeTasaqkgQU1Jlwz6f48dRYpa3BqUSL1QLcZWRyaiTBr7UhAg1EzHWXopLGnHtlWlaCLZiU-EJZKKjJgjTZbOjJ5K-E-LLwFvIc_lcH79-nAtgxXTocmr9im3EUp8_bDKFSR5PIUcUW94-ThY309Q2pkQXS-_FgCLcdyj8tIECkOZk0PBSQmnDYD39UHbKjgVqqa25Fjfc6p7GLJQEPxDXviy_L-Ncw_3nN2HG8QepHrYZw1PIZleBKn1OoAEAcHxHfwdB5LJJ_xwiG5nc-SAxdkBggyfDQHxsDMnPMm8fupg_c2WmZfx6p6VsFi9krX5CwguL3skznTc5Hi3f3sztMjOrDI2_nZ8Cd-JnYCJhCClNkky5VWKZ6UU4uRtflJwei8l_OM-g5op9BVdYoLbUyyI",
    "token": {
        "id": "866016e671437b4c6182e0958cfd4244871023abf84547516221e77703254add355b246338c12b29",
        "user_id": 989,
        "client_id": 246,
        "name": "facebook",
        "scopes": [],
        "revoked": false,
        "created_at": "2018-05-24 15:37:58",
        "updated_at": "2018-05-24 15:37:58",
        "expires_at": "2019-05-24 15:37:58"
    }
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
                "id": 13,
                "user_id": 1,
                "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Blue Color With laptop Compartment",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "BAG15",
                "sku": "BAG15",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "Model Number\tBAG15\r\nItem Height\t15 Centimeters\r\nItem Length\t20 Centimeters\r\nItem Width\t5 Centimeters\r\nVolume Capacity\t20 Liters\r\nItem Weight\t430 Grams\r\nMaterial\tPolyester\r\nSpecial Features\tZip Closure, Shoulder Strap, Laptop Compartment\r\nClosure\tZipper\r\nInner Material\tSatin\r\nStrap\tAdjustable\r\nWarranty Type\tManufacturer",
                "weight": "500.00",
                "length": "40.00",
                "width": "20.00",
                "height": "30.00",
                "amount": "449.00",
                "quantity": 20,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-11-18 19:04:52",
                "updated_at": "2018-05-08 23:02:32",
                "min_price": "449.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": true,
                "brand_name": "TT BAGS",
                "organization": null,
                "media": [
                    {
                        "id": 11,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012127-15-1.jpg",
                        "small": "media/small/1511012127-15-1.jpg",
                        "medium": "media/medium/1511012127-15-1.jpg",
                        "large": "http://localhost:8000/media/large/1511012127-15-1.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 12,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012127-15-2.jpg",
                        "small": "media/small/1511012127-15-2.jpg",
                        "medium": "media/medium/1511012127-15-2.jpg",
                        "large": "http://localhost:8000/media/large/1511012127-15-2.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 13,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012128-15-3.jpg",
                        "small": "media/small/1511012128-15-3.jpg",
                        "medium": "media/medium/1511012128-15-3.jpg",
                        "large": "http://localhost:8000/media/large/1511012128-15-3.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 14,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012129-15-4.jpg",
                        "small": "media/small/1511012129-15-4.jpg",
                        "medium": "media/medium/1511012129-15-4.jpg",
                        "large": "http://localhost:8000/media/large/1511012129-15-4.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 15,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012130-15-5.jpg",
                        "small": "media/small/1511012130-15-5.jpg",
                        "medium": "media/medium/1511012130-15-5.jpg",
                        "large": "http://localhost:8000/media/large/1511012130-15-5.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": null
            },
            {
                "id": 14,
                "user_id": 1,
                "name": "TT Bags Backpacks laptop bag Travel Accessories Fashion Waist Packs Green Color With laptop Compartment",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "BAG16",
                "sku": "BAG16",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "Model Number\tBAG16\r\nItem Height\t15 Centimeters\r\nItem Length\t20 Centimeters\r\nItem Width\t5 Centimeters\r\nVolume Capacity\t20 Liters\r\nItem Weight\t430 Grams\r\nMaterial\tPolyester\r\nSpecial Features\tZip Closure, Shoulder Strap, Laptop Compartment\r\nClosure\tZipper\r\nInner Material\tSatin\r\nStrap\tAdjustable\r\nWarranty Type\tManufacturer",
                "weight": "500.00",
                "length": "40.00",
                "width": "20.00",
                "height": "30.00",
                "amount": "449.00",
                "quantity": 20,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-11-18 19:09:41",
                "updated_at": "2018-05-08 23:02:26",
                "min_price": "449.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": null,
                "media": [
                    {
                        "id": 16,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012497-16-1.jpg",
                        "small": "media/small/1511012497-16-1.jpg",
                        "medium": "media/medium/1511012497-16-1.jpg",
                        "large": "http://localhost:8000/media/large/1511012497-16-1.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 17,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012498-16-2.jpg",
                        "small": "media/small/1511012498-16-2.jpg",
                        "medium": "media/medium/1511012498-16-2.jpg",
                        "large": "http://localhost:8000/media/large/1511012498-16-2.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 18,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012498-16-3.jpg",
                        "small": "media/small/1511012498-16-3.jpg",
                        "medium": "media/medium/1511012498-16-3.jpg",
                        "large": "http://localhost:8000/media/large/1511012498-16-3.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 19,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012499-16-4.jpg",
                        "small": "media/small/1511012499-16-4.jpg",
                        "medium": "media/medium/1511012499-16-4.jpg",
                        "large": "http://localhost:8000/media/large/1511012499-16-4.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 20,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511012500-16-5.jpg",
                        "small": "media/small/1511012500-16-5.jpg",
                        "medium": "media/medium/1511012500-16-5.jpg",
                        "large": "http://localhost:8000/media/large/1511012500-16-5.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": {
                    "id": 35909,
                    "user_id": 759,
                    "product_id": 14,
                    "name": "sakshii bag",
                    "amount": "230.00",
                    "created_at": "2018-05-21 19:08:35",
                    "updated_at": "2018-05-22 11:36:06",
                    "description": ""
                }
            },
            {
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
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": null,
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
            {
                "id": 17,
                "user_id": 1,
                "name": "TT Bags Backpacks laptop bags Travel Accessories Fashion Waist Packs Green Color With laptop Compartment",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "BAG18",
                "sku": "BAG18",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "Model Number\tBAG20\r\nItem Height\t15 Centimeters\r\nItem Length\t20 Centimeters\r\nItem Width\t5 Centimeters\r\nVolume Capacity\t20 Liters\r\nItem Weight\t430 Grams\r\nMaterial\tPolyester\r\nSpecial Features\tZip Closure, Shoulder Strap, Laptop Compartment\r\nClosure\tZipper\r\nInner Material\tSatin\r\nStrap\tAdjustable\r\nWarranty Type\tManufacturer",
                "weight": "500.00",
                "length": "40.00",
                "width": "20.00",
                "height": "30.00",
                "amount": "249.00",
                "quantity": 20,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-11-21 20:09:28",
                "updated_at": "2018-05-08 23:02:14",
                "min_price": "249.00",
                "max_price": "999.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": null,
                "media": [
                    {
                        "id": 29,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511275208-18-1.jpg",
                        "small": "media/small/1511275208-18-1.jpg",
                        "medium": "media/medium/1511275208-18-1.jpg",
                        "large": "http://localhost:8000/media/large/1511275208-18-1.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 30,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511275209-18-2.jpg",
                        "small": "media/small/1511275209-18-2.jpg",
                        "medium": "media/medium/1511275209-18-2.jpg",
                        "large": "http://localhost:8000/media/large/1511275209-18-2.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 31,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511275210-18-3.jpg",
                        "small": "media/small/1511275210-18-3.jpg",
                        "medium": "media/medium/1511275210-18-3.jpg",
                        "large": "http://localhost:8000/media/large/1511275210-18-3.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 32,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511275211-18-4.jpg",
                        "small": "media/small/1511275211-18-4.jpg",
                        "medium": "media/medium/1511275211-18-4.jpg",
                        "large": "http://localhost:8000/media/large/1511275211-18-4.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 33,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1511275211-18-5.jpg",
                        "small": "media/small/1511275211-18-5.jpg",
                        "medium": "media/medium/1511275211-18-5.jpg",
                        "large": "http://localhost:8000/media/large/1511275211-18-5.jpg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": null
            },
            {
                "id": 24,
                "user_id": 1,
                "name": "TT BAGS Mesh Bag Waterproof Backpack (Blue, 20 L)",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "TT Bags12",
                "sku": "Bkpk-16",
                "description": "built for fast moving pursuits, the tt backpack holds all your essential for long day on a trail. It is robust backpack proving protection, the tt bags has a compartment for every need and every accessory It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the tt bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "\r\n\r\nFor Men &amp; Women WaterproofLaptop Backpack\r\n\r\n\r\n",
                "weight": "390.00",
                "length": "15.00",
                "width": "5.00",
                "height": "20.00",
                "amount": "599.00",
                "quantity": 100,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-12-16 14:15:19",
                "updated_at": "2018-03-13 16:16:31",
                "min_price": "599.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": {
                    "id": 1,
                    "user_id": 1,
                    "type_id": 0,
                    "name": "Triple Three Enterprises",
                    "logo": "",
                    "gst": "07AIYPB1269J1ZV",
                    "incorporation_number": "07AIYPB1269J1ZV",
                    "address": "House no.163, No.2 Floor Ground Block - WZ VILLAGE, DASGHARA, NEW DELHI, DELHI, IN, 110012\r\n9810795886",
                    "introduction": "TT Bags is the manufacturer and supplier of wide range of bags such as Backpack, Travelling bags and Duffle bags.",
                    "created_at": "2017-11-18 18:46:56",
                    "updated_at": "2018-03-29 14:44:24",
                    "city": "Delhi",
                    "state": "Delhi",
                    "pincode": "110012",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 117,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513596154-bkpk-16-tt-bags-20-original-imaetcgj6mbspdph.jpeg",
                        "small": "media/small/1513596154-bkpk-16-tt-bags-20-original-imaetcgj6mbspdph.jpeg",
                        "medium": "media/medium/1513596154-bkpk-16-tt-bags-20-original-imaetcgj6mbspdph.jpeg",
                        "large": "http://localhost:8000/media/large/1513596154-bkpk-16-tt-bags-20-original-imaetcgj6mbspdph.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": null
            },
            {
                "id": 25,
                "user_id": 1,
                "name": "TT BAGS Mesh Bag Waterproof Backpack (Blue, 20 L)",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "TT Bags13",
                "sku": "Bkpk-2",
                "description": "built for fast moving pursuits, the tt backpack holds all your essential for long day on a trail. It is robust backpack proving protection, the tt bags has a compartment for every need and every accessory It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the tt bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "\r\n\r\nFor Men &amp; Women WaterproofLaptop Backpack\r\n\r\n\r\n",
                "weight": "390.00",
                "length": "15.00",
                "width": "5.00",
                "height": "20.00",
                "amount": "449.00",
                "quantity": 100,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-12-16 14:15:19",
                "updated_at": "2018-02-23 12:22:43",
                "min_price": "449.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": {
                    "id": 1,
                    "user_id": 1,
                    "type_id": 0,
                    "name": "Triple Three Enterprises",
                    "logo": "",
                    "gst": "07AIYPB1269J1ZV",
                    "incorporation_number": "07AIYPB1269J1ZV",
                    "address": "House no.163, No.2 Floor Ground Block - WZ VILLAGE, DASGHARA, NEW DELHI, DELHI, IN, 110012\r\n9810795886",
                    "introduction": "TT Bags is the manufacturer and supplier of wide range of bags such as Backpack, Travelling bags and Duffle bags.",
                    "created_at": "2017-11-18 18:46:56",
                    "updated_at": "2018-03-29 14:44:24",
                    "city": "Delhi",
                    "state": "Delhi",
                    "pincode": "110012",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 127,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513597761-bkpk-2-tt-bags-20-original-imaetcgg5w8pkzvc.jpeg",
                        "small": "media/small/1513597761-bkpk-2-tt-bags-20-original-imaetcgg5w8pkzvc.jpeg",
                        "medium": "media/medium/1513597761-bkpk-2-tt-bags-20-original-imaetcgg5w8pkzvc.jpeg",
                        "large": "http://localhost:8000/media/large/1513597761-bkpk-2-tt-bags-20-original-imaetcgg5w8pkzvc.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 128,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513597801-bkpk-2-tt-bags-20-original-imaetcggyy2pekbu.jpeg",
                        "small": "media/small/1513597801-bkpk-2-tt-bags-20-original-imaetcggyy2pekbu.jpeg",
                        "medium": "media/medium/1513597801-bkpk-2-tt-bags-20-original-imaetcggyy2pekbu.jpeg",
                        "large": "http://localhost:8000/media/large/1513597801-bkpk-2-tt-bags-20-original-imaetcggyy2pekbu.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 129,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513597813-bkpk-2-tt-bags-20-original-imaetcgguchjd8v3.jpeg",
                        "small": "media/small/1513597813-bkpk-2-tt-bags-20-original-imaetcgguchjd8v3.jpeg",
                        "medium": "media/medium/1513597813-bkpk-2-tt-bags-20-original-imaetcgguchjd8v3.jpeg",
                        "large": "http://localhost:8000/media/large/1513597813-bkpk-2-tt-bags-20-original-imaetcgguchjd8v3.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 130,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513597822-bkpk-2-tt-bags-20-original-imaetcggtexg24zu.jpeg",
                        "small": "media/small/1513597822-bkpk-2-tt-bags-20-original-imaetcggtexg24zu.jpeg",
                        "medium": "media/medium/1513597822-bkpk-2-tt-bags-20-original-imaetcggtexg24zu.jpeg",
                        "large": "http://localhost:8000/media/large/1513597822-bkpk-2-tt-bags-20-original-imaetcggtexg24zu.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 131,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513597832-bkpk-2-tt-bags-20-original-imaetcggr2t2xjgj.jpeg",
                        "small": "media/small/1513597832-bkpk-2-tt-bags-20-original-imaetcggr2t2xjgj.jpeg",
                        "medium": "media/medium/1513597832-bkpk-2-tt-bags-20-original-imaetcggr2t2xjgj.jpeg",
                        "large": "http://localhost:8000/media/large/1513597832-bkpk-2-tt-bags-20-original-imaetcggr2t2xjgj.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": null
            },
            {
                "id": 30,
                "user_id": 1,
                "name": "TT BAGS Backpack 2.5 L Laptop Backpack (Black)",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "TT Bags14",
                "sku": "BAG03",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "\r\n\r\nFor Men &amp; Women WaterproofLaptop Backpack\r\n\r\n\r\n",
                "weight": "390.00",
                "length": "15.00",
                "width": "5.00",
                "height": "20.00",
                "amount": "599.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-12-16 15:57:50",
                "updated_at": "2018-03-13 16:11:30",
                "min_price": "599.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": {
                    "id": 1,
                    "user_id": 1,
                    "type_id": 0,
                    "name": "Triple Three Enterprises",
                    "logo": "",
                    "gst": "07AIYPB1269J1ZV",
                    "incorporation_number": "07AIYPB1269J1ZV",
                    "address": "House no.163, No.2 Floor Ground Block - WZ VILLAGE, DASGHARA, NEW DELHI, DELHI, IN, 110012\r\n9810795886",
                    "introduction": "TT Bags is the manufacturer and supplier of wide range of bags such as Backpack, Travelling bags and Duffle bags.",
                    "created_at": "2017-11-18 18:46:56",
                    "updated_at": "2018-03-29 14:44:24",
                    "city": "Delhi",
                    "state": "Delhi",
                    "pincode": "110012",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 132,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598095-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd45cjzkyhz.jpeg",
                        "small": "media/small/1513598095-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd45cjzkyhz.jpeg",
                        "medium": "media/medium/1513598095-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd45cjzkyhz.jpeg",
                        "large": "http://localhost:8000/media/large/1513598095-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd45cjzkyhz.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 133,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598102-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4jvbx8znb.jpeg",
                        "small": "media/small/1513598102-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4jvbx8znb.jpeg",
                        "medium": "media/medium/1513598102-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4jvbx8znb.jpeg",
                        "large": "http://localhost:8000/media/large/1513598102-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4jvbx8znb.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 134,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598108-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4mhtaqmst.jpeg",
                        "small": "media/small/1513598108-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4mhtaqmst.jpeg",
                        "medium": "media/medium/1513598108-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4mhtaqmst.jpeg",
                        "large": "http://localhost:8000/media/large/1513598108-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4mhtaqmst.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 135,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598114-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd47xtfjbbk.jpeg",
                        "small": "media/small/1513598114-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd47xtfjbbk.jpeg",
                        "medium": "media/medium/1513598114-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd47xtfjbbk.jpeg",
                        "large": "http://localhost:8000/media/large/1513598114-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd47xtfjbbk.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 136,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598120-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4pgjdq4za.jpeg",
                        "small": "media/small/1513598120-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4pgjdq4za.jpeg",
                        "medium": "media/medium/1513598120-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4pgjdq4za.jpeg",
                        "large": "http://localhost:8000/media/large/1513598120-backpack-tt1-laptop-backpack-tt-bags-original-imaetmd4pgjdq4za.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": null
            },
            {
                "id": 32,
                "user_id": 1,
                "name": "TT Bags Bkpk-21 15 L Backpack (Orange)",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "TT Bags16",
                "sku": "Bkpk-21",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "\r\n\r\nFor Men &amp; Women WaterproofLaptop Backpack\r\n\r\n\r\n",
                "weight": "390.00",
                "length": "15.00",
                "width": "5.00",
                "height": "20.00",
                "amount": "299.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-12-16 15:57:50",
                "updated_at": "2018-02-23 12:21:30",
                "min_price": "299.00",
                "max_price": "999.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": {
                    "id": 1,
                    "user_id": 1,
                    "type_id": 0,
                    "name": "Triple Three Enterprises",
                    "logo": "",
                    "gst": "07AIYPB1269J1ZV",
                    "incorporation_number": "07AIYPB1269J1ZV",
                    "address": "House no.163, No.2 Floor Ground Block - WZ VILLAGE, DASGHARA, NEW DELHI, DELHI, IN, 110012\r\n9810795886",
                    "introduction": "TT Bags is the manufacturer and supplier of wide range of bags such as Backpack, Travelling bags and Duffle bags.",
                    "created_at": "2017-11-18 18:46:56",
                    "updated_at": "2018-03-29 14:44:24",
                    "city": "Delhi",
                    "state": "Delhi",
                    "pincode": "110012",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 142,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598471-bkpk-21-bag8-backpack-tt-bags-original-imaevmkggcumfmgh.jpeg",
                        "small": "media/small/1513598471-bkpk-21-bag8-backpack-tt-bags-original-imaevmkggcumfmgh.jpeg",
                        "medium": "media/medium/1513598471-bkpk-21-bag8-backpack-tt-bags-original-imaevmkggcumfmgh.jpeg",
                        "large": "http://localhost:8000/media/large/1513598471-bkpk-21-bag8-backpack-tt-bags-original-imaevmkggcumfmgh.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 143,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598477-bkpk-21-bag8-backpack-tt-bags-original-imaevmkghagq6juw.jpeg",
                        "small": "media/small/1513598477-bkpk-21-bag8-backpack-tt-bags-original-imaevmkghagq6juw.jpeg",
                        "medium": "media/medium/1513598477-bkpk-21-bag8-backpack-tt-bags-original-imaevmkghagq6juw.jpeg",
                        "large": "http://localhost:8000/media/large/1513598477-bkpk-21-bag8-backpack-tt-bags-original-imaevmkghagq6juw.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 144,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598483-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgbym2dger.jpeg",
                        "small": "media/small/1513598483-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgbym2dger.jpeg",
                        "medium": "media/medium/1513598483-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgbym2dger.jpeg",
                        "large": "http://localhost:8000/media/large/1513598483-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgbym2dger.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 145,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598500-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgkf8adhyx.jpeg",
                        "small": "media/small/1513598500-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgkf8adhyx.jpeg",
                        "medium": "media/medium/1513598500-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgkf8adhyx.jpeg",
                        "large": "http://localhost:8000/media/large/1513598500-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgkf8adhyx.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 146,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598513-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgyzgdg5ma.jpeg",
                        "small": "media/small/1513598513-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgyzgdg5ma.jpeg",
                        "medium": "media/medium/1513598513-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgyzgdg5ma.jpeg",
                        "large": "http://localhost:8000/media/large/1513598513-bkpk-21-bag8-backpack-tt-bags-original-imaevmkgyzgdg5ma.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": {
                    "id": 35245,
                    "user_id": 759,
                    "product_id": 32,
                    "name": "TT Bags Bkpk-21 15 L Backpack (Orange)",
                    "amount": "299.00",
                    "created_at": "2018-05-10 21:46:17",
                    "updated_at": "2018-05-10 21:46:17",
                    "description": ""
                }
            },
            {
                "id": 33,
                "user_id": 1,
                "name": "TT BAGS Backpack 2.5 L Laptop Backpack (Blue)",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "TT Bags17",
                "sku": "BAG07",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "\r\n\r\nFor Men &amp; Women WaterproofLaptop Backpack\r\n\r\n\r\n",
                "weight": "390.00",
                "length": "15.00",
                "width": "5.00",
                "height": "20.00",
                "amount": "499.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-12-16 15:57:50",
                "updated_at": "2018-03-13 16:14:08",
                "min_price": "499.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": {
                    "id": 1,
                    "user_id": 1,
                    "type_id": 0,
                    "name": "Triple Three Enterprises",
                    "logo": "",
                    "gst": "07AIYPB1269J1ZV",
                    "incorporation_number": "07AIYPB1269J1ZV",
                    "address": "House no.163, No.2 Floor Ground Block - WZ VILLAGE, DASGHARA, NEW DELHI, DELHI, IN, 110012\r\n9810795886",
                    "introduction": "TT Bags is the manufacturer and supplier of wide range of bags such as Backpack, Travelling bags and Duffle bags.",
                    "created_at": "2017-11-18 18:46:56",
                    "updated_at": "2018-03-29 14:44:24",
                    "city": "Delhi",
                    "state": "Delhi",
                    "pincode": "110012",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 147,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598707-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4zcwxwyg8.jpeg",
                        "small": "media/small/1513598707-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4zcwxwyg8.jpeg",
                        "medium": "media/medium/1513598707-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4zcwxwyg8.jpeg",
                        "large": "http://localhost:8000/media/large/1513598707-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4zcwxwyg8.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 148,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598746-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4e3ees82y.jpeg",
                        "small": "media/small/1513598746-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4e3ees82y.jpeg",
                        "medium": "media/medium/1513598746-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4e3ees82y.jpeg",
                        "large": "http://localhost:8000/media/large/1513598746-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4e3ees82y.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 149,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598760-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4v2wjmgtk.jpeg",
                        "small": "media/small/1513598760-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4v2wjmgtk.jpeg",
                        "medium": "media/medium/1513598760-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4v2wjmgtk.jpeg",
                        "large": "http://localhost:8000/media/large/1513598760-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4v2wjmgtk.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 150,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513598769-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4pkqvmhmm.jpeg",
                        "small": "media/small/1513598769-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4pkqvmhmm.jpeg",
                        "medium": "media/medium/1513598769-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4pkqvmhmm.jpeg",
                        "large": "http://localhost:8000/media/large/1513598769-backpack-tt3-laptop-backpack-tt-bags-original-imaetmd4pkqvmhmm.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": null
            },
            {
                "id": 34,
                "user_id": 1,
                "name": "TT BAGS Mesh Bag Waterproof Backpack (Red, 20 L)",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "TT Bags18",
                "sku": "Bkpk-12",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "For Men &amp; Women WaterproofLaptop Backpack\r\n",
                "weight": "390.00",
                "length": "15.00",
                "width": "5.00",
                "height": "20.00",
                "amount": "849.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-12-16 15:57:50",
                "updated_at": "2018-02-23 12:29:55",
                "min_price": "849.00",
                "max_price": "1999.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": {
                    "id": 1,
                    "user_id": 1,
                    "type_id": 0,
                    "name": "Triple Three Enterprises",
                    "logo": "",
                    "gst": "07AIYPB1269J1ZV",
                    "incorporation_number": "07AIYPB1269J1ZV",
                    "address": "House no.163, No.2 Floor Ground Block - WZ VILLAGE, DASGHARA, NEW DELHI, DELHI, IN, 110012\r\n9810795886",
                    "introduction": "TT Bags is the manufacturer and supplier of wide range of bags such as Backpack, Travelling bags and Duffle bags.",
                    "created_at": "2017-11-18 18:46:56",
                    "updated_at": "2018-03-29 14:44:24",
                    "city": "Delhi",
                    "state": "Delhi",
                    "pincode": "110012",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 151,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513600641-bkpk-12-tt-bags-20-original-imaet9ahfey2rhvx.jpeg",
                        "small": "media/small/1513600641-bkpk-12-tt-bags-20-original-imaet9ahfey2rhvx.jpeg",
                        "medium": "media/medium/1513600641-bkpk-12-tt-bags-20-original-imaet9ahfey2rhvx.jpeg",
                        "large": "http://localhost:8000/media/large/1513600641-bkpk-12-tt-bags-20-original-imaet9ahfey2rhvx.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 152,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513600650-bkpk-12-tt-bags-20-original-imaet9ahntbe9fzd.jpeg",
                        "small": "media/small/1513600650-bkpk-12-tt-bags-20-original-imaet9ahntbe9fzd.jpeg",
                        "medium": "media/medium/1513600650-bkpk-12-tt-bags-20-original-imaet9ahntbe9fzd.jpeg",
                        "large": "http://localhost:8000/media/large/1513600650-bkpk-12-tt-bags-20-original-imaet9ahntbe9fzd.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 153,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513600667-bkpk-12-tt-bags-20-original-imaet9ahbjf9xvza.jpeg",
                        "small": "media/small/1513600667-bkpk-12-tt-bags-20-original-imaet9ahbjf9xvza.jpeg",
                        "medium": "media/medium/1513600667-bkpk-12-tt-bags-20-original-imaet9ahbjf9xvza.jpeg",
                        "large": "http://localhost:8000/media/large/1513600667-bkpk-12-tt-bags-20-original-imaet9ahbjf9xvza.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 154,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513600675-bkpk-12-tt-bags-20-original-imaet9ahggpgfzys.jpeg",
                        "small": "media/small/1513600675-bkpk-12-tt-bags-20-original-imaet9ahggpgfzys.jpeg",
                        "medium": "media/medium/1513600675-bkpk-12-tt-bags-20-original-imaet9ahggpgfzys.jpeg",
                        "large": "http://localhost:8000/media/large/1513600675-bkpk-12-tt-bags-20-original-imaet9ahggpgfzys.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 155,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513600685-bkpk-12-tt-bags-20-original-imaet9ahz6ghw2wd.jpeg",
                        "small": "media/small/1513600685-bkpk-12-tt-bags-20-original-imaet9ahz6ghw2wd.jpeg",
                        "medium": "media/medium/1513600685-bkpk-12-tt-bags-20-original-imaet9ahz6ghw2wd.jpeg",
                        "large": "http://localhost:8000/media/large/1513600685-bkpk-12-tt-bags-20-original-imaet9ahz6ghw2wd.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": null
            },
            {
                "id": 35,
                "user_id": 1,
                "name": "TT BAGS Mesh Bag Waterproof Backpack (Grey, 20 L)",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "TT Bags19",
                "sku": "Bkpk-8",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "\r\n\r\nFor Men &amp; Women WaterproofLaptop Backpack\r\n\r\n\r\n\r\n",
                "weight": "390.00",
                "length": "15.00",
                "width": "5.00",
                "height": "20.00",
                "amount": "449.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-12-16 15:57:50",
                "updated_at": "2018-02-23 12:16:51",
                "min_price": "449.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": {
                    "id": 1,
                    "user_id": 1,
                    "type_id": 0,
                    "name": "Triple Three Enterprises",
                    "logo": "",
                    "gst": "07AIYPB1269J1ZV",
                    "incorporation_number": "07AIYPB1269J1ZV",
                    "address": "House no.163, No.2 Floor Ground Block - WZ VILLAGE, DASGHARA, NEW DELHI, DELHI, IN, 110012\r\n9810795886",
                    "introduction": "TT Bags is the manufacturer and supplier of wide range of bags such as Backpack, Travelling bags and Duffle bags.",
                    "created_at": "2017-11-18 18:46:56",
                    "updated_at": "2018-03-29 14:44:24",
                    "city": "Delhi",
                    "state": "Delhi",
                    "pincode": "110012",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 156,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659487-bkpk-8-tt-bags-20-original-imaet9ah54fy6bz9.jpeg",
                        "small": "media/small/1513659487-bkpk-8-tt-bags-20-original-imaet9ah54fy6bz9.jpeg",
                        "medium": "media/medium/1513659487-bkpk-8-tt-bags-20-original-imaet9ah54fy6bz9.jpeg",
                        "large": "http://localhost:8000/media/large/1513659487-bkpk-8-tt-bags-20-original-imaet9ah54fy6bz9.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 158,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659522-bkpk-8-tt-bags-20-original-imaet9aheadfqhah.jpeg",
                        "small": "media/small/1513659522-bkpk-8-tt-bags-20-original-imaet9aheadfqhah.jpeg",
                        "medium": "media/medium/1513659522-bkpk-8-tt-bags-20-original-imaet9aheadfqhah.jpeg",
                        "large": "http://localhost:8000/media/large/1513659522-bkpk-8-tt-bags-20-original-imaet9aheadfqhah.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 159,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659527-bkpk-8-tt-bags-20-original-imaet9ah8ehdyz6h.jpeg",
                        "small": "media/small/1513659527-bkpk-8-tt-bags-20-original-imaet9ah8ehdyz6h.jpeg",
                        "medium": "media/medium/1513659527-bkpk-8-tt-bags-20-original-imaet9ah8ehdyz6h.jpeg",
                        "large": "http://localhost:8000/media/large/1513659527-bkpk-8-tt-bags-20-original-imaet9ah8ehdyz6h.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 160,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659535-bkpk-8-tt-bags-20-original-imaet9ahffhxkgza.jpeg",
                        "small": "media/small/1513659535-bkpk-8-tt-bags-20-original-imaet9ahffhxkgza.jpeg",
                        "medium": "media/medium/1513659535-bkpk-8-tt-bags-20-original-imaet9ahffhxkgza.jpeg",
                        "large": "http://localhost:8000/media/large/1513659535-bkpk-8-tt-bags-20-original-imaet9ahffhxkgza.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 161,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659541-bkpk-8-tt-bags-20-original-imaet9ahbv8utkfq.jpeg",
                        "small": "media/small/1513659541-bkpk-8-tt-bags-20-original-imaet9ahbv8utkfq.jpeg",
                        "medium": "media/medium/1513659541-bkpk-8-tt-bags-20-original-imaet9ahbv8utkfq.jpeg",
                        "large": "http://localhost:8000/media/large/1513659541-bkpk-8-tt-bags-20-original-imaet9ahbv8utkfq.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": null
            },
            {
                "id": 36,
                "user_id": 1,
                "name": "TT BAGS Backpack 2.5 L Laptop Backpack (Black)",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "TT Bags20",
                "sku": "BAG01",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "\r\n\r\nFor Men &amp; Women&nbsp;WaterproofCapacity: 2.5 L",
                "weight": "390.00",
                "length": "15.00",
                "width": "5.00",
                "height": "20.00",
                "amount": "499.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-12-16 15:57:50",
                "updated_at": "2018-03-13 16:15:40",
                "min_price": "499.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": {
                    "id": 1,
                    "user_id": 1,
                    "type_id": 0,
                    "name": "Triple Three Enterprises",
                    "logo": "",
                    "gst": "07AIYPB1269J1ZV",
                    "incorporation_number": "07AIYPB1269J1ZV",
                    "address": "House no.163, No.2 Floor Ground Block - WZ VILLAGE, DASGHARA, NEW DELHI, DELHI, IN, 110012\r\n9810795886",
                    "introduction": "TT Bags is the manufacturer and supplier of wide range of bags such as Backpack, Travelling bags and Duffle bags.",
                    "created_at": "2017-11-18 18:46:56",
                    "updated_at": "2018-03-29 14:44:24",
                    "city": "Delhi",
                    "state": "Delhi",
                    "pincode": "110012",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 162,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659736-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd45kccngtd.jpeg",
                        "small": "media/small/1513659736-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd45kccngtd.jpeg",
                        "medium": "media/medium/1513659736-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd45kccngtd.jpeg",
                        "large": "http://localhost:8000/media/large/1513659736-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd45kccngtd.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 163,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659744-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4edkeextz.jpeg",
                        "small": "media/small/1513659744-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4edkeextz.jpeg",
                        "medium": "media/medium/1513659744-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4edkeextz.jpeg",
                        "large": "http://localhost:8000/media/large/1513659744-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4edkeextz.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 164,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659766-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4fzbcacn5.jpeg",
                        "small": "media/small/1513659766-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4fzbcacn5.jpeg",
                        "medium": "media/medium/1513659766-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4fzbcacn5.jpeg",
                        "large": "http://localhost:8000/media/large/1513659766-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4fzbcacn5.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 165,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659773-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4wvw6p2gz.jpeg",
                        "small": "media/small/1513659773-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4wvw6p2gz.jpeg",
                        "medium": "media/medium/1513659773-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4wvw6p2gz.jpeg",
                        "large": "http://localhost:8000/media/large/1513659773-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4wvw6p2gz.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 166,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659779-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4xyq6s6j6.jpeg",
                        "small": "media/small/1513659779-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4xyq6s6j6.jpeg",
                        "medium": "media/medium/1513659779-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4xyq6s6j6.jpeg",
                        "large": "http://localhost:8000/media/large/1513659779-backpack-tts1-laptop-backpack-tt-bags-original-imaetmd4xyq6s6j6.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": null
            },
            {
                "id": 37,
                "user_id": 1,
                "name": "TT BAGS Backpack 2.5 L Laptop Backpack (Red)",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "TT Bags21",
                "sku": "BAG21",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "\r\n\r\nFor Men &amp; Women WaterproofLaptop Backpack\r\n\r\n\r\n",
                "weight": "390.00",
                "length": "15.00",
                "width": "5.00",
                "height": "20.00",
                "amount": "249.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-12-16 15:57:50",
                "updated_at": "2018-02-23 12:24:06",
                "min_price": "249.00",
                "max_price": "999.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": {
                    "id": 1,
                    "user_id": 1,
                    "type_id": 0,
                    "name": "Triple Three Enterprises",
                    "logo": "",
                    "gst": "07AIYPB1269J1ZV",
                    "incorporation_number": "07AIYPB1269J1ZV",
                    "address": "House no.163, No.2 Floor Ground Block - WZ VILLAGE, DASGHARA, NEW DELHI, DELHI, IN, 110012\r\n9810795886",
                    "introduction": "TT Bags is the manufacturer and supplier of wide range of bags such as Backpack, Travelling bags and Duffle bags.",
                    "created_at": "2017-11-18 18:46:56",
                    "updated_at": "2018-03-29 14:44:24",
                    "city": "Delhi",
                    "state": "Delhi",
                    "pincode": "110012",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 167,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659982-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4fakgqfq4.jpeg",
                        "small": "media/small/1513659982-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4fakgqfq4.jpeg",
                        "medium": "media/medium/1513659982-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4fakgqfq4.jpeg",
                        "large": "http://localhost:8000/media/large/1513659982-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4fakgqfq4.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 168,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659988-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4gnh6aqsy.jpeg",
                        "small": "media/small/1513659988-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4gnh6aqsy.jpeg",
                        "medium": "media/medium/1513659988-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4gnh6aqsy.jpeg",
                        "large": "http://localhost:8000/media/large/1513659988-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4gnh6aqsy.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 169,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513659994-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4hmnzzjmb.jpeg",
                        "small": "media/small/1513659994-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4hmnzzjmb.jpeg",
                        "medium": "media/medium/1513659994-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4hmnzzjmb.jpeg",
                        "large": "http://localhost:8000/media/large/1513659994-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4hmnzzjmb.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 170,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513660000-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4vkbtzxez.jpeg",
                        "small": "media/small/1513660000-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4vkbtzxez.jpeg",
                        "medium": "media/medium/1513660000-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4vkbtzxez.jpeg",
                        "large": "http://localhost:8000/media/large/1513660000-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4vkbtzxez.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 171,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513660007-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4qwpdnfxg.jpeg",
                        "small": "media/small/1513660007-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4qwpdnfxg.jpeg",
                        "medium": "media/medium/1513660007-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4qwpdnfxg.jpeg",
                        "large": "http://localhost:8000/media/large/1513660007-backpack-tt7-laptop-backpack-tt-bags-original-imaetmd4qwpdnfxg.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": null
            },
            {
                "id": 38,
                "user_id": 1,
                "name": "TT BAGS Duffle Bags Travel Duffel Bag (Black)",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "TT Bags22",
                "sku": "BAG31",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "\r\n\r\nFor Men &amp; Women Waterproof\r\n\r\n",
                "weight": "390.00",
                "length": "15.00",
                "width": "5.00",
                "height": "20.00",
                "amount": "349.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-12-16 15:57:50",
                "updated_at": "2018-03-06 13:16:18",
                "min_price": "349.00",
                "max_price": "999.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": {
                    "id": 1,
                    "user_id": 1,
                    "type_id": 0,
                    "name": "Triple Three Enterprises",
                    "logo": "",
                    "gst": "07AIYPB1269J1ZV",
                    "incorporation_number": "07AIYPB1269J1ZV",
                    "address": "House no.163, No.2 Floor Ground Block - WZ VILLAGE, DASGHARA, NEW DELHI, DELHI, IN, 110012\r\n9810795886",
                    "introduction": "TT Bags is the manufacturer and supplier of wide range of bags such as Backpack, Travelling bags and Duffle bags.",
                    "created_at": "2017-11-18 18:46:56",
                    "updated_at": "2018-03-29 14:44:24",
                    "city": "Delhi",
                    "state": "Delhi",
                    "pincode": "110012",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 172,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513660125-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6pehh6hfr.jpeg",
                        "small": "media/small/1513660125-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6pehh6hfr.jpeg",
                        "medium": "media/medium/1513660125-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6pehh6hfr.jpeg",
                        "large": "http://localhost:8000/media/large/1513660125-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6pehh6hfr.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 173,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513660132-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6q8dmkhv3.jpeg",
                        "small": "media/small/1513660132-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6q8dmkhv3.jpeg",
                        "medium": "media/medium/1513660132-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6q8dmkhv3.jpeg",
                        "large": "http://localhost:8000/media/large/1513660132-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6q8dmkhv3.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 174,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513660138-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp66rychvux.jpeg",
                        "small": "media/small/1513660138-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp66rychvux.jpeg",
                        "medium": "media/medium/1513660138-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp66rychvux.jpeg",
                        "large": "http://localhost:8000/media/large/1513660138-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp66rychvux.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 175,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513660149-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6bruakmxq.jpeg",
                        "small": "media/small/1513660149-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6bruakmxq.jpeg",
                        "medium": "media/medium/1513660149-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6bruakmxq.jpeg",
                        "large": "http://localhost:8000/media/large/1513660149-duffle-bags-bag3-travel-duffel-bag-tt-bags-original-imaevhp6bruakmxq.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
                "categories": [
                    {
                        "id": 104,
                        "name": "Luggage & Bags - Luggage & Travel Bags",
                        "description": "",
                        "meta_title": "",
                        "meta_des": "",
                        "meta_keywords": "",
                        "slug": "",
                        "parent_id": null,
                        "status": 1
                    }
                ],
                "user_product": null
            },
            {
                "id": 39,
                "user_id": 1,
                "name": "TT BAGS Mesh Bag Waterproof Backpack (Black, Grey, 20 L)",
                "slug": "",
                "bdpin": "",
                "brand_id": 1,
                "model": "TT Bags23",
                "sku": "Bkpk-14",
                "description": "Built for fast moving pursuits, the TT Backpack holds all your essential for long day on a trail. It is robust backpack proving protection, It comes equipped with a large padded pocket, internal and external accessory pouches which zip for extra security Comfort was also no sacrifice in the design of this backpack. To ensure that you keep going on your journey throughout the day, the TT bags has two padded adjustable shoulder straps and a padded back panel. You will hardly know you are wearing it! And when you finally stop to take a rest, this backpack will securely stand upright to ensure none of your products are damaged when you set it down.",
                "specification": "\r\n\r\nFor Men &amp; Women WaterproofLaptop Backpack\r\n\r\n\r\n",
                "weight": "390.00",
                "length": "15.00",
                "width": "5.00",
                "height": "20.00",
                "amount": "549.00",
                "quantity": 10,
                "status": 1,
                "source": "bigly",
                "source_id": null,
                "created_at": "2017-12-16 15:57:50",
                "updated_at": "2018-02-23 12:29:04",
                "min_price": "549.00",
                "max_price": "1299.00",
                "shipping_charge": "75.00",
                "attributes": [],
                "isWishlist": false,
                "brand_name": "TT BAGS",
                "organization": {
                    "id": 1,
                    "user_id": 1,
                    "type_id": 0,
                    "name": "Triple Three Enterprises",
                    "logo": "",
                    "gst": "07AIYPB1269J1ZV",
                    "incorporation_number": "07AIYPB1269J1ZV",
                    "address": "House no.163, No.2 Floor Ground Block - WZ VILLAGE, DASGHARA, NEW DELHI, DELHI, IN, 110012\r\n9810795886",
                    "introduction": "TT Bags is the manufacturer and supplier of wide range of bags such as Backpack, Travelling bags and Duffle bags.",
                    "created_at": "2017-11-18 18:46:56",
                    "updated_at": "2018-03-29 14:44:24",
                    "city": "Delhi",
                    "state": "Delhi",
                    "pincode": "110012",
                    "country": "India"
                },
                "media": [
                    {
                        "id": 176,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513660236-bkpk-14-tt-bags-20-original-imaetcggxrg3me6r.jpeg",
                        "small": "media/small/1513660236-bkpk-14-tt-bags-20-original-imaetcggxrg3me6r.jpeg",
                        "medium": "media/medium/1513660236-bkpk-14-tt-bags-20-original-imaetcggxrg3me6r.jpeg",
                        "large": "http://localhost:8000/media/large/1513660236-bkpk-14-tt-bags-20-original-imaetcggxrg3me6r.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 177,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513660241-bkpk-14-tt-bags-20-original-imaetcggjnh9rx6v.jpeg",
                        "small": "media/small/1513660241-bkpk-14-tt-bags-20-original-imaetcggjnh9rx6v.jpeg",
                        "medium": "media/medium/1513660241-bkpk-14-tt-bags-20-original-imaetcggjnh9rx6v.jpeg",
                        "large": "http://localhost:8000/media/large/1513660241-bkpk-14-tt-bags-20-original-imaetcggjnh9rx6v.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 178,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513660247-bkpk-14-tt-bags-20-original-imaetcggqvrjyfas.jpeg",
                        "small": "media/small/1513660247-bkpk-14-tt-bags-20-original-imaetcggqvrjyfas.jpeg",
                        "medium": "media/medium/1513660247-bkpk-14-tt-bags-20-original-imaetcggqvrjyfas.jpeg",
                        "large": "http://localhost:8000/media/large/1513660247-bkpk-14-tt-bags-20-original-imaetcggqvrjyfas.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 179,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513660253-bkpk-14-tt-bags-20-original-imaetcgghncaj2d9.jpeg",
                        "small": "media/small/1513660253-bkpk-14-tt-bags-20-original-imaetcgghncaj2d9.jpeg",
                        "medium": "media/medium/1513660253-bkpk-14-tt-bags-20-original-imaetcgghncaj2d9.jpeg",
                        "large": "http://localhost:8000/media/large/1513660253-bkpk-14-tt-bags-20-original-imaetcgghncaj2d9.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    },
                    {
                        "id": 180,
                        "mime": "image/jpeg",
                        "thumb": "media/thumb/1513660260-bkpk-14-tt-bags-20-original-imaetcggbpy9athx.jpeg",
                        "small": "media/small/1513660260-bkpk-14-tt-bags-20-original-imaetcggbpy9athx.jpeg",
                        "medium": "media/medium/1513660260-bkpk-14-tt-bags-20-original-imaetcggbpy9athx.jpeg",
                        "large": "http://localhost:8000/media/large/1513660260-bkpk-14-tt-bags-20-original-imaetcggbpy9athx.jpeg",
                        "caption": null,
                        "default": 0,
                        "check": "pending"
                    }
                ],
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
                "user_product": null
            }
        ],
        "from": 1,
        "last_page": 623,
        "next_page_url": "http://localhost:8000/api/products?page=2",
        "path": "http://localhost:8000/api/products",
        "per_page": 15,
        "prev_page_url": null,
        "to": 15,
        "total": 9332
    },
    "filter": {
        "categories": [
            {
                "id": 179,
                "name": "Bike & Car-Accessories"
            },
            {
                "id": 167,
                "name": "Books"
            },
            {
                "id": 50,
                "name": "Camera & Photo"
            },
            {
                "id": 41,
                "name": "Computer Accessories"
            },
            {
                "id": 49,
                "name": "Electronic Accessories"
            },
            {
                "id": 58,
                "name": "Electronic appliances"
            },
            {
                "id": 6,
                "name": "Health & Personal Care"
            },
            {
                "id": 19,
                "name": "Herbs & Seasonings"
            },
            {
                "id": 43,
                "name": "Holi Colour"
            },
            {
                "id": 171,
                "name": "Home & Décor - Curtains"
            },
            {
                "id": 42,
                "name": "Home & Decor- Accessories"
            },
            {
                "id": 170,
                "name": "Home & Decor-Cushion Cover & Bedsheet"
            },
            {
                "id": 157,
                "name": "Jewellery"
            },
            {
                "id": 72,
                "name": "Jewelry Packaging & Display"
            },
            {
                "id": 44,
                "name": "Kitchen Masala"
            },
            {
                "id": 100,
                "name": "Luggage & Bags - Backpacks"
            },
            {
                "id": 103,
                "name": "Luggage & Bags - Handbags"
            },
            {
                "id": 104,
                "name": "Luggage & Bags - Luggage & Travel Bags"
            },
            {
                "id": 155,
                "name": "Luggage & Bags - Office Bags"
            },
            {
                "id": 156,
                "name": "Luggage & Bags - Sling Bags"
            },
            {
                "id": 105,
                "name": "Luggage & Bags - Special Purpose Bags"
            },
            {
                "id": 107,
                "name": "Luggage & Bags - Waist Packs"
            },
            {
                "id": 108,
                "name": "Luggage & Bags - Wallets & Holders"
            },
            {
                "id": 55,
                "name": "Men's Clothing"
            },
            {
                "id": 33,
                "name": "Mobile Accessories"
            },
            {
                "id": 151,
                "name": "Office and Stationary"
            },
            {
                "id": 172,
                "name": "Organic Products - Cleaners"
            },
            {
                "id": 173,
                "name": "Others"
            },
            {
                "id": 35,
                "name": "Pot Plant"
            },
            {
                "id": 97,
                "name": "Shoes - Men's Shoes"
            },
            {
                "id": 60,
                "name": "Smart Electronics"
            },
            {
                "id": 150,
                "name": "Sunglasses"
            },
            {
                "id": 32,
                "name": "Watch"
            },
            {
                "id": 62,
                "name": "Women's Clothing"
            },
            {
                "id": 183,
                "name": "Womens Ethnic Wear"
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
    "faqs": [
        {
            "que": "{\"What is Bigly\"",
            "ans": "\"BigLy is Ecommerce platform tool\""
        },
        {
            "que": "\"What is pricing\"",
            "ans": "\"Goto app.bigly.io\\/pricing to check pricing\"}"
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
    "faqs": [
        {
            "que": "{\"What is Bigly\"",
            "ans": "\"BigLy is Ecommerce platform tool\""
        },
        {
            "que": "\"What is pricing\"",
            "ans": "\"Goto app.bigly.io\\/pricing to check pricing\"}"
        }
    ]
}
```



