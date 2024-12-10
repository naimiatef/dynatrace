# Dynatrace – Analyses de problèmes- Niveau 1
## Objectif
- Ce document permet de suivre pas à pas la démarche d’investigation de certains types de problème
- Les démarches décrites sont valables pour un serveur Dynatrace
- Il conviendra toujours en premier lieu d’ouvrir le détail du problème détecté

![image](https://github.com/user-attachments/assets/0866ee37-1968-40c2-858f-e74ed4b1f11d)
![image](https://github.com/user-attachments/assets/dbc05b1c-6a42-472b-b45e-e16dfece266a)
![image](https://github.com/user-attachments/assets/7c8d978d-cfe5-4bc5-8a8a-a3f9b1823bb4)
![image](https://github.com/user-attachments/assets/2cbcadd2-05df-4de5-97ca-2552ab898a2d)
![image](https://github.com/user-attachments/assets/c241f579-1f8b-45ab-9fbe-fdae9e4ceca1)
![image](https://github.com/user-attachments/assets/f53fa1c3-bc61-4b79-8dee-5b54a89fdc5d)
![image](https://github.com/user-attachments/assets/53d0f2a9-96c5-4031-b0d7-c1a9720f90c4)
![image](https://github.com/user-attachments/assets/2f2ffb20-4753-4406-b157-23fcca0df282)
![image](https://github.com/user-attachments/assets/89d94222-6096-4a80-999d-dfa6c076a7ef)
![image](https://github.com/user-attachments/assets/37cf180a-b3af-4483-8ffc-6f349bab3231)
![image](https://github.com/user-attachments/assets/28922f1c-6f44-49ab-bc80-9ecc9120b103)
![image](https://github.com/user-attachments/assets/56dbf1f8-c072-4213-b4f6-d9e176e30639)
![image](https://github.com/user-attachments/assets/8900c57e-e4a6-43f4-aa67-42babcbe86ef)
![image](https://github.com/user-attachments/assets/9668c0b8-1fed-4767-a142-15d02e151a84)
![image](https://github.com/user-attachments/assets/b21fef0b-fef3-46fd-a408-0dcfd12eecfd)
![image](https://github.com/user-attachments/assets/eaeff5e1-a124-4653-8798-3e365af13d89)
![image](https://github.com/user-attachments/assets/18f44c78-190d-4346-b7d9-0e1040497c05)
![image](https://github.com/user-attachments/assets/7d2f5a66-fa61-4f19-9a38-9ac9bae1cf76)
![image](https://github.com/user-attachments/assets/06f3a5ac-c06f-41e1-bfdb-069934a7a1d6)
![image](https://github.com/user-attachments/assets/06a2e247-502c-4d76-8215-bdb6912eaca4)
![image](https://github.com/user-attachments/assets/2e968609-409c-4d4a-bc6d-25c7a1b15227)
![image](https://github.com/user-attachments/assets/d9e67afb-17b5-447e-85be-d3713d7156da)
![image](https://github.com/user-attachments/assets/b731360b-854e-43d1-ac25-f2f3a9aa853a)
![image](https://github.com/user-attachments/assets/5c308c4f-4c2c-43e0-b9b7-8b192724f88b)
![image](https://github.com/user-attachments/assets/f66f611b-1d5f-483f-9993-197490d6c8c0)
![image](https://github.com/user-attachments/assets/cb4bd68a-aaca-4299-b808-54090a523025)
![image](https://github.com/user-attachments/assets/8e96b875-80f3-44a8-8c13-4872a029beb9)
![image](https://github.com/user-attachments/assets/89679176-6278-4b82-abb5-3f3fbf5d80d5)
![image](https://github.com/user-attachments/assets/c238ce78-4f91-47f9-87bf-ea3a4dd46aa2)
![image](https://github.com/user-attachments/assets/55abddf7-4f4a-4f33-a4ec-0ca03fba0f58)
![image](https://github.com/user-attachments/assets/5bc6b70a-ce7c-40f6-931f-92ecb3547e20)
![image](https://github.com/user-attachments/assets/d3dd15a4-1b4e-427b-b95a-27eafb835294)
![image](https://github.com/user-attachments/assets/d828726b-d355-4748-bd71-b71839825e8c)
![image](https://github.com/user-attachments/assets/72a42e1f-a4c6-4868-a439-3ee618c26244)
![image](https://github.com/user-attachments/assets/b526edb4-55dd-4bb9-a396-d0f99081b9cd)
![image](https://github.com/user-attachments/assets/48f45f8b-0686-4e58-a97a-c1e51c570c85)
![image](https://github.com/user-attachments/assets/d1dfaa67-dec8-4c2c-8725-91dabeab11bf)
![image](https://github.com/user-attachments/assets/6355026e-bbc7-4991-8fd7-eb123065d31f)
![image](https://github.com/user-attachments/assets/0807119b-7545-4375-82ba-07223ee3ffff)
![image](https://github.com/user-attachments/assets/6d3af28f-813a-416f-bcb5-77aa6c2bd6c8)
![image](https://github.com/user-attachments/assets/f95306f8-f86f-4a6b-8d25-7b5db31a27e8)
![image](https://github.com/user-attachments/assets/fa2c2c4c-6c5b-48dc-ac8b-7b17b5d9d14c)
![image](https://github.com/user-attachments/assets/9a749052-7a7b-490b-85e3-0980f3e5eea8)
![image](https://github.com/user-attachments/assets/9cd90293-4c46-448c-8a00-c3c37d15fdda)
![image](https://github.com/user-attachments/assets/fa5fc443-ad0b-40c5-b75f-62c16bb8452b)
![image](https://github.com/user-attachments/assets/e088d523-20be-41c1-9e5f-d966159205ee)
![image](https://github.com/user-attachments/assets/ab7f78f9-7872-4451-9fc0-3d426c72d580)
![image](https://github.com/user-attachments/assets/84232e83-346f-400d-84f7-35e013958746)
![image](https://github.com/user-attachments/assets/b5a72a6b-4e79-4761-8141-2128c29bb073)
![image](https://github.com/user-attachments/assets/a7772605-5b9e-4341-a214-a66870fa6b6b)
![image](https://github.com/user-attachments/assets/d6a1e7bd-5df1-42db-bafc-e4bdb8ed58ca)
![image](https://github.com/user-attachments/assets/0b2de551-e24a-45bd-abfe-b034139cd77e)
![image](https://github.com/user-attachments/assets/a7013ef3-7bd7-4898-a1db-be3475518ba5)






















































