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

![リソース整備状況](documents/sap_rmq_list.drawio.png)

## sap-sandbox-rmq における SAP領域・機能 の選択基準
sap-sandbox-rmq におけるSAP領域・機能は、SAP S4HANA のあらゆる領域・機能のうち、世界中の企業で繰り返し利用される、利用頻度の高いものと判断されるものが、選択されています。

## Port 番号 の 適用方針 
| type      | Area         | ポート番号    |
| :-------- | :----------------------------- | :---------------------------------------- |
| NodePort  | Central Functions              | 50503-50510 |
|           | Logistics             |    50511-50515    |
|           | Inventory Management |          50516-50525                                 |
|           | Sales Management |50526-50540|
|           | Procurement Management           |             50541-50550                              |
|           | Production Management          |          50551-50560                                 |
|           | Process Management           |            50561-50565                               |
|           | Quality Management          |                50566-50570                           |
|           | Plant Maintenance        |                 50571-50585                          |
|           | Customer Service         |                 50586-50590           |
