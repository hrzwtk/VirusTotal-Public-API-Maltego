# [VirusTotal Public API] Maltego Local Transforms
Maltego Local Transform to use VirusTotal Public API - https://www.virustotal.com/en/documentation/public-api/

# Prerequisites
- VirusTotal Public API access
- Python 2.7.x + requests, json, random module
- Python 3.6.x will probably work.

# 必要なもの
- VirusTotal Public APIのアクセス権
- Python 2.7.x + requests, json, random モジュール
- Python 3.6.x でもたぶん動作します。

# Setup
- Edit VTPub.py and set "apikey" variable with your API key. If you have multiple API keys, you can set them to increase quota.  
- Put all python files into your working directory. (e.g. C:\Maltego\Transforms\VirusTotal_Public)  
- Open VTPub.mtz to import Maltego configuration.  
- The current configuration uses the following directories, so you may have to change them according to your environment. (Maltego -> Transforms -> Transform Manager)  

  Command line = C:\Python27\python.exe  
  Working directory = C:\Maltego\Transforms\VirusTotal_Public

# セットアップ
- VTPub.py の中で、\<Your API Key\> の箇所に自分の API key を記載してください。複数の API key を持っている場合は、クォータを増やすために複数記載することもできます。
- 全てのPythonファイルを、このTransform用に作ったディレクトリに置いてください。（例： C:\Maltego\Transforms\VirusTotal_Public）
- VTPub.mtz を開いて、Maltegoの設定をインポートしてください。
- mtzファイルに含まれる設定では、下記のディレクトリが指定されていますが、自分の環境に合わせて変更してください。（Maltego -> Transforms -> Transform Manager）

  Command line = C:\Python27\python.exe  
  Working directory = C:\Maltego\Transforms\VirusTotal_Public

# Transforms
- [VTPub] domain_reports  
Input: Domain  
Output: Sub domains, Detected communicationg hashes, Detected downloaded hashes, Detected URLs, IP addresses, Categories  
<img src="https://user-images.githubusercontent.com/16297449/42561148-73596bb6-8533-11e8-8317-9597649dbb7b.png" width="900">

- [VTPub] ip_reports  
Input: IP address  
Output: Detected communicating hashes, Detected downloaded hashes, Detected URLs, Domains, Country  
<img src="https://user-images.githubusercontent.com/16297449/42553927-e4149f58-851d-11e8-8da9-b9f016fca3ba.png" width="900">

- [VTPub] url_reports  
Input: URL  
Output: Detection ratio  
<img src="https://user-images.githubusercontent.com/16297449/42554036-45812b76-851e-11e8-9433-0f6752fbb09e.png" width="300">

- [VTPub] file_reports  
Input: Hash  
Output: Detection ratio, Detection names  
<img src="https://user-images.githubusercontent.com/16297449/42554097-806b25fc-851e-11e8-8a4b-f55c5d21afbc.png" width="600">

- [VTPub] file_rescan  
Input: Hash  
Output: N/A  
<img src="https://user-images.githubusercontent.com/16297449/42554137-a5f3b62c-851e-11e8-92f9-fd78897d12b5.png" width="300">

- [VTPub] url_scan  
Input: URL  
Output: N/A  
<img src="https://user-images.githubusercontent.com/16297449/42554170-d013c74e-851e-11e8-9878-0bda03af6816.png" width="300">

- [VTPub] md5  
Input: Hash  
Output: MD5 Hash  
<img src="https://user-images.githubusercontent.com/16297449/42554224-053c3bd6-851f-11e8-8852-41462cf24621.png" width="300">

- [VTPub] sha256  
Input: Hash  
Output: SHA256 Hash  
<img src="https://user-images.githubusercontent.com/16297449/42554238-0e2a422e-851f-11e8-8785-62640ad7e845.png" width="300">
