# eev
e version tools, stored in 10.5.10-MariaDB-1:10.5.10+maria~focal 

# table

CREATE TABLE eev0y (eid int not null primary key, arr JSON COMPRESSED) engine = myisam;
CREATE TABLE eev (eid int not null primary key, arr JSON COMPRESSED) ENGINE=MRG_MyISAM DEFAULT CHARSET=utf8 INSERT_METHOD=LAST UNION=(`eev0y`,`eev1y`,`eev2y`);
CREATE TABLE eevsnts (eid int not null primary key, arr JSON COMPRESSED) ENGINE=MRG_MyISAM DEFAULT CHARSET=utf8 INSERT_METHOD=LAST UNION=(`eev0y_snts`,`eev1y_snts`,`eev2y_snts`);

# sample data 

root@192.168.1.24|eevone>select * from eev limit 1000,1 \G
*************************** 1. row ***************************
eid: 4869
arr: {"2": [2467, 4869, 10422, 0, 0, "The Panda's Weeping Cry", "\n As we know, there are many endangous species in the world, their amout were decreasing and panda is of them.pandas only exist in china, most of them live in SiChuang province, ShanXi province and GanSu province,until \r\n\nnow,2011,just 1600 were survived no matter how the experts to protect them, they just decreaseing and we can on- \r\n\nly regret why we didn't take measures to pretect them before. \r\n\n The amout of pandas also can influent by the environment that they live , pandas like eat bamboo ,but with the deforesting , bamboo were cut down and wild pandas didn't have enought foood to eat , so many of them were starve to death . We should protect them , not only the pandas , but also the environment they live , we should keep in mind that once pandas extincted , they eill never come back again , don't let them extinct because human's mistake. ", "<P>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; As we know, there are many endangous species in the world, their amout were decreasing and panda is of them.pandas only exist in china, most of them live in SiChuang province, ShanXi province and GanSu province,until </P>\r\n<P>now,2011,just 1600 were survived no matter how the experts to protect them, they just decreaseing and we can on-</P>\r\n<P>ly regret why we didn't take measures to pretect them before.</P>\r\n<P>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;The amout of pandas also can influent by the environment that they live , pandas like eat bamboo ,but with the deforesting , bamboo were cut down and wild pandas didn't have enought foood to eat , so many of them were starve to death . We should protect them , not only the pandas , but also the environment they live , we should keep in mind that once pandas extincted , they eill never come back again , don't let them extinct because human's mistake.</P>", "2011-03-12 20:40:53", 2533, 0, 0, 0, 1299933653, "10101021014", "\u90d1\u70b3\u676d", "10\u7ea7A29\u73ed", 0, 0.0, 0.0, 0.0, "", 0, 0.0, 0, 2, 0, "", 0, 0, "", 0, "", 0, ""]}
1 row in set (0.01 sec)
