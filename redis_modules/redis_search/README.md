* How to List Indexes: FT._LIST
* Create Index: FT.CREATE idx:transaction ON HASH PREFIX 1 transaction_ SCHEMA status as status TEXT location as location TEXT
* Insert some data: hset transaction_1 amount 100 status success date 2023-11-07 location mumbai
* Insert some data: hset transaction_2 amount 200 status failed date 2023-11-07 location mumbai
* Insert some data: hset transaction_3 amount 1001 status failed date 2023-11-07 location delhi
* Insert some data: hset transaction_4 amount 1010 status failed date 2023-11-07 location delhi
* Insert some data: hset transaction_5 amount 200 status success date 2023-11-07 location delhi
* Insert some data: hset transaction_6 amount 2001 status success date 2023-11-07 location hyd
* Insert some data: hset transaction_7 amount 556 status processing date 2023-11-07 location hyd
* Insert some data: hset transaction_8 amount 891 status processing date 2023-11-07 location hyd

* Get all transactions WHERE status = failed: FT.SEARCH idx:transaction "@status:success"
* Get all transactions WHERE location = mumbai: FT.SEARCH idx:transaction "@location:mumbai"
* Get all transactions WHERE location is mumbai OR hyd: FT.SEARCH idx:transaction "@location:mumbai | @location:hyd"
