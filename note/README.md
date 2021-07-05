+++
title = "基本的なAppSyncのDynamo DBリゾルバ"
date = "2021-04-13"
tags = ["AppSync", "Dynamo DB"]
+++

とりあえずDynamo DBをAppSyncでクエリしてみるだけ、という、もうこれ以上どうにもならないほどに簡単なものを作った。最初の第一歩みたいなものだ。

[Githubのリポジトリ](https://github.com/suzukiken/cdkappsync-dynamo)

とりあえずDynamo DBのテーブルが1つ、idがプライマリキーで、フィールド（Dynamo DB的にはattribute）がtitleのみ。
GraphQLはレコード（Dynamo DB的にはitem）を

* get
* list
* add
* delete

ができるというだけ。

認証はApiKeyにしている。これがもしIAMでも、どっちにしてもAWSコンソールのAppSyncのクエリのページで動作は確認できる。

![img](/img/2021/04/appsync-dynamo-query.png)
