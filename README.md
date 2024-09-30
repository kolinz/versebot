# versebot
Difyを前提に作成するメタバースの活用および構築支援チャットボットドキュメント

# 概要
生成AIサービス開発プラットフォームの「Dify」を使っています。「Dify」はオープンソースソフトウェアで、SaaS版もありますが、IBM Cloud Virtual Serverなどの仮想サーバーを用意することで、自社運用ができます。
本研究で試作した試作チャットボット「Versebot」は、RAG(Retrieval Augmented Generation) を活用しています。Difyでは、ナレッジ機能に文書をアップロードすることで、Dify上で開発するチャットボットに対して、RAGを付与することが可能です。

IBM Cloud Virtual Server上の仮想マシンを使って、Difyを実装することができます。IBM CloudにDifyを導入する方法は、下記ドキュメントをご覧ください。
[DifyをIBM Cloud Virtual Serverで動かして、IBM Cloudについて質問できる基本のチャットボットを作るまで #ibmcloud - Qiita](https://qiita.com/kolinz/items/a27976f19f28fd4829d9)

## 試作チャットボットの再現方法
Difyでは定義ファイル「DSLファイル」を使って、既に作成済みのアプリケーションを再現することができます。RAGを使っていますので、「ナレッジ機能」を使い下図のように文書を登録する必要があります。[文書](https://github.com/kolinz/versebot/tree/main/rag/knowledges)を１つ１つ登録後、DSLインポートを行ってください。
DSLファイルのインポートには、[公式ドキュメント](https://docs.dify.ai/v/ja-jp/guides/application-orchestrate/creating-an-application)をご覧ください。

## フロントエンドをカスタマイズする場合
Difyのフロントエンドアプリケーションをカスタマイズし、IBM Cloud Code Engine 上で動かすことも可能です。Difyの見た目をカスタマイズしたい場合は、下記のドキュメントを参考に、IBM Cloud Code Engineを使って実装することを推奨します。
[Difyのカスタムクライアント「webapp-conversation」をIBM Cloud Code Engineで動かすまでの手順 #ibmcloud - Qiita](https://qiita.com/kolinz/items/e55456e94d914165a186)



# 著作権表記
本資料の著作権は、日本アイ・ビー・エム株式会社（IBM Corporationを含み、以下、IBMといいます。）に帰属します。
ワークショップ、セッション、および資料は、IBMまたはセッション発表者によって準備され、それぞれ独自の見解を反映したものです。
それらは情報提供の目的のみで提供されており、いかなる参加者に対しても法律的またはその他の指導や助言を意図したものではなく、またそのような結果を生むものでもありません。本資料に含まれている情報については、完全性と正確性を期するよう努力しましたが、「現
状のまま」提供され、明示または暗示にかかわらずいかなる保証も伴わないものとします。本資料またはその他の資料の使用によって、あるいはその他の関連によって、いかなる損害が生じた場合も、IBMまたはセッション発表者は責任を負わないものとします。 本資料に含ま
れている内容は、IBMまたはそのサプライヤーやライセンス交付者からいかなる保証または表明を引きだすことを意図したものでも、IBMソフトウェアの使用を規定する適用ライセンス契約の条項を変更することを意図したものでもなく、またそのような結果を生むものでもあ
りません。
本資料でIBM製品、プログラム、またはサービスに言及していても、IBMが営業活動を行っているすべての国でそれらが使用可能であることを暗示するものではありません。本資料で言及している製品リリース日付や製品機能は、市場機会またはその他の要因に基づいてIBM独自の決定権をもっていつでも変更できるものとし、いかなる方法においても将来の製品または機能が使用可能になると確約することを意図したものではありません。本資料に含まれている内容は、参加者が開始する活動によって特定の販売、売上高の向上、またはその他の結果
が生じると述べる、または暗示することを意図したものでも、またそのような結果を生むものでもありません。 パフォーマンスは、管理された環境において標準的なIBMベンチマークを使用した測定と予測に基づいています。ユーザーが経験する実際のスループットやパフォー
マンスは、ユーザーのジョブ・ストリームにおけるマルチプログラミングの量、入出力構成、ストレージ構成、および処理されるワークロードなどの考慮事項を含む、数多くの要因に応じて変化します。したがって、個々のユーザーがここで述べられているものと同様の結果を得られると確約するものではありません。
記述されているすべてのお客様事例は、それらのお客様がどのようにIBM製品を使用したか、またそれらのお客様が達成した結果の実例として示されたものです。実際の環境コストおよびパフォーマンス特性は、お客様ごとに異なる場合があります。
IBM、IBM ロゴは、 米国やその他の国におけるInternational Business Machines Corporationの商標または登録商標です。他の製品名およびサービス名等は、それぞれIBMまたは各社の商標である場合があります。現時点での IBM の商標リストについては、
ibm.com/trademarkをご覧ください。

