# 第6回 解答

## 演習

<!-- [tool call] の行は、表示された行をそのまま貼り付けてください。終わらなかった STEP は、空欄のままでかまいません。 -->

- STEP 1 のツールの名前：glossary_search_glossary
- STEP 2 の [tool call]：glossary_search_glossary({'query': '3レベル'})
- STEP 3 の [tool call]：fetch_fetch({'url': 'https://modelcontextprotocol.io/'})
- STEP 4 の [tool call]：aws_aws___search_documentation({'search_phrase': 'Amazon S3 バージョニング 概要', 'topics': ['general']})、aws_aws___search_documentation({'topics': ['general'], 'search_phrase': '"Using versioning" "Amazon S3" overview'})
- 気づき・疑問：STEP3では、MCPの公式サイトを読みに行った。URLを自分のホームページに変更して概要を依頼したところ、依頼どおり自動アクセスして概要が得られた。STEP4では、AWSのMCPサーバを使用して、AWSのヘルプを得ることができた。

## 宿題

<!-- 基礎・実装・発展のどれか1つに取り組めば完了です。 -->

- 取り組んだレベル：基礎 
- やったこと：app/mcp_server.pyに、server.tool()(tools.get_lecture_summary)を記載した。
- 結果：サーバー側を変更するだけで、エージェント側のapp.mcp_agentのに見えるツール一覧に[glossary_get_lecture_summary]が追加された。第2回で学ぶ質問をすると、「glossary_get_lecture_summary」が呼ばれた。
- 気づき・疑問：glossary_get_lecture_summary　がなくても、モデルは第2回で学ぶ内容を、そのほかのツールや一般知識を使用して回答したと思われるが、精度はそれなりであり、内容は保証されないと考える。


