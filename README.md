hello

0215_9 Backup EC2 Volumes Automate Creating Snapshots

results: PS C:\Users\manny\OneDrive\Desktop\AWS> & c:/Users/manny/OneDrive/Desktop/AWS/.venv/Scripts/python.exe "c:/Users/manny/OneDrive/Desktop/AWS/.venv/cleanup snapshots.py"
[{'Description': '', 'Encrypted': False, 'OwnerId': '774305607671', 'Progress': '100%', 'SnapshotId': 'snap-0894730c062e9bbc5', 'StartTime': datetime.datetime(2024, 9, 27, 20, 35, 36, 637000, tzinfo=tzutc()), 'State': 'completed', 'VolumeId': 'vol-06f03e6c839e59d77', 'VolumeSize': 8, 'StorageTier': 'standard'}, {'Description': '', 'Encrypted': False, 'OwnerId': '774305607671', 'Progress': '100%', 'SnapshotId': 'snap-0483ce9981ac48dbe', 'StartTime': datetime.datetime(2024, 9, 27, 20, 30, 0, 893000, tzinfo=tzutc()), 'State': 'completed', 'VolumeId': 'vol-06f03e6c839e59d77', 'VolumeSize': 8, 'StorageTier': 'standard'}, {'Description': '', 'Encrypted': False, 'OwnerId': '774305607671', 'Progress': '100%', 'SnapshotId': 'snap-0c2c8e6b72185a72f', 'StartTime': datetime.datetime(2024, 9, 27, 20, 35, 36, 348000, tzinfo=tzutc()), 'State': 'completed', 'VolumeId': 'vol-0e80f8add7da425b4', 'VolumeSize': 8, 'StorageTier': 'standard'}, {'Description': '', 'Encrypted': False, 'OwnerId': '774305607671', 'Progress': '100%', 'SnapshotId': 'snap-04149ce8402c90ac1', 'StartTime': datetime.datetime(2024, 9, 27, 20, 31, 52, 401000, tzinfo=tzutc()), 'State': 'completed', 'VolumeId': 'vol-06f03e6c839e59d77', 'VolumeSize': 8, 'StorageTier': 'standard'}, {'Description': '', 'Encrypted': False, 'OwnerId': '774305607671', 'Progress': '100%', 'SnapshotId': 'snap-0b113cb47a34e8c56', 'StartTime': datetime.datetime(2024, 9, 27, 20, 29, 5, 179000, tzinfo=tzutc()), 'State': 'completed', 'VolumeId': 'vol-06f03e6c839e59d77', 'VolumeSize': 8, 'StorageTier': 'standard'}, {'Description': '', 'Encrypted': False, 'OwnerId': '774305607671', 'Progress': '100%', 'SnapshotId': 'snap-0e3f98c8d8e20b8c0', 'StartTime': datetime.datetime(2024, 9, 27, 20, 31, 52, 113000, tzinfo=tzutc()), 'State': 'completed', 'VolumeId': 'vol-0e80f8add7da425b4', 'VolumeSize': 8, 'StorageTier': 'standard'}]




Snapshots by start time

top results not in order. bottom results in order from earliest start time

results:
2024-09-27 20:35:36.637000+00:00
2024-09-27 20:30:00.893000+00:00
2024-09-27 20:35:36.348000+00:00
2024-09-27 20:31:52.401000+00:00
2024-09-27 20:29:05.179000+00:00
2024-09-27 20:31:52.113000+00:00
###########
2024-09-27 20:29:05.179000+00:00
2024-09-27 20:30:00.893000+00:00
2024-09-27 20:31:52.113000+00:00
2024-09-27 20:31:52.401000+00:00
2024-09-27 20:35:36.348000+00:00
2024-09-27 20:35:36.637000+00:00

add to line 10 - reverse=True - this make the start time descend

2024-09-27 20:35:36.637000+00:00
2024-09-27 20:35:36.348000+00:00
2024-09-27 20:31:52.401000+00:00
2024-09-27 20:31:52.113000+00:00
2024-09-27 20:30:00.893000+00:00
2024-09-27 20:29:05.179000+00:00




Most current snapshots only


PS C:\Users\manny\OneDrive\Desktop\AWS> & c:/Users/manny/OneDrive/Desktop/AWS/.venv/Scripts/python.exe "c:/Users/manny/OneDrive/Desktop/AWS/.venv/cleanup snapshots.py"
{'ResponseMetadata': {'RequestId': '86ca105a-dd1b-4f07-9430-be8d2ef3617d', 'HTTPStatusCode': 200, 'HTTPHeaders': {'x-amzn-requestid': '86ca105a-dd1b-4f07-9430-be8d2ef3617d', 'cache-control': 'no-cache, no-store', 'strict-transport-security': 'max-age=31536000; includeSubDomains', 'content-type': 'text/xml;charset=UTF-8', 'content-length': '217', 'date': 'Sat, 28 Sep 2024 00:29:44 GMT', 'server': 'AmazonEC2'}, 'RetryAttempts': 0}}
{'ResponseMetadata': {'RequestId': 'd2c4edd4-475e-4198-8c41-13216d9a29c3', 'HTTPStatusCode': 200, 'HTTPHeaders': {'x-amzn-requestid': 'd2c4edd4-475e-4198-8c41-13216d9a29c3', 'cache-control': 'no-cache, no-store', 'strict-transport-security': 'max-age=31536000; includeSubDomains', 'content-type': 'text/xml;charset=UTF-8', 'content-length': '217', 'date': 'Sat, 28 Sep 2024 00:29:44 GMT', 'server': 'AmazonEC2'}, 'RetryAttempts': 0}}
{'ResponseMetadata': {'RequestId': '0d30204c-697f-4ead-a594-2ba5d3136d60', 'HTTPStatusCode': 200, 'HTTPHeaders': {'x-amzn-requestid': '0d30204c-697f-4ead-a594-2ba5d3136d60', 'cache-control': 'no-cache, no-store', 'strict-transport-security': 'max-age=31536000; includeSubDomains', 'content-type': 'text/xml;charset=UTF-8', 'content-length': '217', 'date': 'Sat, 28 Sep 2024 00:29:44 GMT', 'server': 'AmazonEC2'}, 'RetryAttempts': 0}}
{'ResponseMetadata': {'RequestId': 'cd086829-935a-4d6f-93e5-2a0ac26b359f', 'HTTPStatusCode': 200, 'HTTPHeaders': {'x-amzn-requestid': 'cd086829-935a-4d6f-93e5-2a0ac26b359f', 'cache-control': 'no-cache, no-store', 'strict-transport-security': 'max-age=31536000; includeSubDomains', 'content-type': 'text/xml;charset=UTF-8', 'content-length': '217', 'date': 'Sat, 28 Sep 2024 00:29:44 GMT', 'server': 'AmazonEC2'}, 'RetryAttempts': 0}}

![[Pasted image 20240927203207.png]]
