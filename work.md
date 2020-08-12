1. 采购人测试账户 ：

    cgr_zqy@163.com 

    111111

2. 供应商测试账户：  

​         gys_ceshi@qq.com

3. svn://47.95.210.220/zzzc/purchase

4. http://test.365trade.com.cn/qicaitong/

5. gg_czyb  用户表

6. TAPD:

   845369629@qq.com

   19930831Zxd

7. 码云:

   15010482214

   19930831zxd

8. 订单和客户管理

# 中招合约

1. 客户频道

   账户:   jjsunle@hotmail.com 

​          密码:  admin

2. 合约用户管理

   账户:admin

   密码:admin









## 2020-4-14

测试：

1. 物品采购申请--->审批日志:sql执行错误(已修改，DqgzFacadeImpl.670)

2. 物品类型管理:(sql执行错误,已修改,LsIndex.218;  已修改,数据问题,wp_wplx)

3. 物品领用申请

     a.选择费用类别树，选完后，选择树不自动消失

     b.添加品类，按钮保存并提交审核和暂存不提交,点击无反应

##2020-4-15

物品领用申请

  a.选择费用类别树，选完后，选择树不自动消失

  b. 添加品类，按钮保存并提交审核和暂存不提交,点击无反应

​                  （已解决50%，可以保存成功信息。

​                      保存成功后页面无跳转；

​                      可以多次保存)

  c.物品领用申请---->查看详细信息，无信息显示(已解决)

##2020-4-16

1. 物品领用申请

     a.选择费用类别树，选完后，选择树不自动消失(已解决)

     b. 添加品类，按钮保存并提交审核和暂存不提交,点击无反应(已解决)

​                  （已解决,可以保存成功信息。

​                      未解决,保存成功后页面无跳转；)

2. 竞拍流程测试完成，正常流程可走通

## 2020-4-17

1. 熟悉中招合约项目
2. 测试物品管理

## 2020-4-21

1. 商品管理---分类管理-->上传、新增、修改、删除，已实现可用
2. 商品管理---分类管理-->导出，不可用
3. 商品管理---分类管理-->上架，下架没找到

## 2020-4-23

T_XT_角色表

//super 角色以及权限
 INSERT INTO T_XT_JS_CD
(UUID,JS_DM,CD_DM,LR_SJ,LRRY_DM)
VALUES
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','32cc598160614fc7bfb80130aac4d371','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','c98a4273-21c8-441f-b520-3e2465d168b3','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','100','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','a817f020-f06d-4318-a2f2-5fa54fff8628','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','63759c2c-b0ce-4814-98fa-0efc574c4fb0','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','8a12d7eb768340c3abbb1f8890559e6a','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','fe17117551ef492a834399a7c6cf2eca','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','100100','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','05ebc3b1-eefb-43f9-8d22-8284749191d3','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','100100100','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','1b8d1c1056a845139422f783bed2cdf5','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','f8d96cc6b9cb4c98a0f278d460a74215','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','55446ee25cdc45ec89b9bd41f9151831','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','c650f8d859b14899b74956b67be2ea5b','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','4d7df62f3a1d4251abc79830010c2cfe','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','3dd440df554e4b2eb95f2fd74c003d67','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','6eb15e27963c418b95e7b79938640c0a','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','4771beedc3014c9ca5610bfb53454af8','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','deb9822a-0a01-4b90-ab42-15237297a776','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','90f79711-3d17-421e-b2b2-e27d8d28a9d4','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','57f1a82145e0401a9bdc61ff23ea8a85','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','08b452b4-8b04-4fc2-9b01-579d53a6e0f4','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','27c10ba2-2b86-4f4d-a3c2-8d403dd39b0e','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','91f4f73a-3f69-4354-8fbe-281eb717ddcb','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','643b8fffb43940b683288f94fd903b29','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','cd703b5298454c218f8823c8fff01a1e','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','acd58294-9581-45d2-b6cc-9eb02d2faa26','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','ee7e434e-f2e1-45cc-9c81-935677fcdff3','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','15eb1d40cff24b89a67779bc2b35a57e','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','9825a76c3f7248039880d01feb7b0d60','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','24c8f9bdf8e94641b613065fa674b6d0','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','8ed5c381f88342579b0e3fa80a1335eb','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','2ac3a960-3f2c-4f65-85c5-f21896d2ecb3','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','efdbbe3a-3594-4e41-af25-57b7ec8fcd30','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','2aa8d537ca194f87b670830243bb90db','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','17ad57e94b214828b9310ef74eaab9cd','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','e50987bb6333406b9c78c92a7d1ab1ad','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','9eee50a94731491181a266a7b52bf6b6','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','b916330d698e4bc782a63c515a00358a','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','6353feb2d9fe42779693a54993ac19d2','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','22324928058247608490a68911316c17','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','80c1b05b59bb4e4394aae1137983e4f4','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','b5beb5a3-d065-4275-b36d-b169d290d574','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','555e94c0-432a-47d8-a048-4e798e22a9c2','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','967e0ebedbee42c2b868136b036a980a','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','82c28bbefb834d4287d9724c072e93d7','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','def8c58e30954c588c4f687f48326efe','2017-03-31 10:34:19','admin'),
('cbb393c19a66461f86844a7bce825ba0','44fee0acc43e4b19a77dcfe21bad979a','a2729dc74b3b455c9d05b7357c92a10b','2017-03-31 10:34:19','admin')

    ## 2020-4-24

特殊订单：

1.下单，需要审批流程，没有无法下单

## 2020-4-26

1. 普通商品分类管理

## 2020-4-27

1. 内部会议

    a.商城

    b. 自采

## 2020-4-28

 测试url

http://localhost:8083/categorynormalmgr/categorynormal/categoryMgr.do

## 2020-4-30

1. 修改用户 后台拉取数据慢，











  

