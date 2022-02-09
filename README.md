<p align="center"> <img src="https://user-images.githubusercontent.com/91356865/144049159-1ebbd095-87d2-4a3c-81cb-277cc1d4c7b7.png" width="300"> </p> <p align="center"> Starting Up the API Environment on a "Full-of-Beans" SandBox </p>

***

# sap-sandbox-rmq
sap-sandbox-rmq は、[sap-sandbox](https://github.com/latonaio/sap-sandbox) における API READS の内、RabbitMQ からのメッセージを受けてイベントドリブンでランタイムを実行し、アウトプットとしてRabbitMQへメッセージを出力するよう対応されたリソースをまとめたリポジトリです。  
sap-sandbox の 「sandbox」は、Netflix 韓国ドラマ 「START-UP」 より、すべての開発者のための 地ならし になればという想いから命名されました。  
なお、各リポジトリのリソースは、そのままクラウド環境におけるアプリケーションにも適用可能です。  

## 前提条件  
sap-sandbox-rmq は、オンプレミス版である（＝クラウド版ではない）SAPS4HANA API の利用を前提としています。  
クラウド版APIを利用する場合は、ご注意ください。

## Latona における SAP 領域・機能ごと の リソース整備状況    
下の図において、チェックマークが付いているリソースが、Latonaにおいて(少なくとも1次の)整備が行われたものであり、github上に公開されています。  

![リソース整備状況](documents/sap_sandbox.rmq.drawio.png)

## sap-sandbox-rmq における SAP領域・機能 の選択基準
sap-sandbox-rmq におけるSAP領域・機能は、SAP S4HANA のあらゆる領域・機能のうち、世界中の企業で繰り返し利用される、利用頻度の高いものと判断されるものが、選択されています。

## Port 番号 の 適用方針 
| type      | Area         | ポート番号    |
| :-------- | :----------------------------- | :---------------------------------------- |
| NodePort  | Central Functions              | 30503-30510 |
|           | Logistics             |    30511-30515    |
|           | Inventory Management |          30516-30525                                 |
|           | Sales Management |30526-30540|
|           | Procurement Management           |             30541-30550                              |
|           | Production Management          |          30551-30560                                 |
|           | Process Management           |            30561-30565                               |
|           | Quality Management          |                30566-30570                           |
|           | Plant Maintenance        |                 30571-30585                          |
|           | Customer Service         |                 30586-30590           |
