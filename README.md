X-ray goggles on Node.js
========================

This is a reboot of the xray goggles, so that it is served as a node app.

**NOTE: This README assumes that you have all the required external dependencies installed and have a working dev environment. New to Webmaker? Make sure to read our [developer guide](https://wiki.mozilla.org/Webmaker/Code) for everything you need in order to get started!**

Prequisites
-----------

* [make-valet](https://github.com/mozilla/make-valet)

Migration
---------

Various scripts are present that will assist in migrating old data sets along with Node.js scripts to update old records.

* `migrations/09052013-add-makeid-column.sql`
    * Used to add the `makeid` to the `ThimbleProject` data model. Using the script will depend on your SQL managing environment, but here's an example of using it in a commandline prompt:
        * `mysql < migrations/09052013-add-makeid-column.sql` - Assumes you have already done `use <DB_NAME>`

* `migrations/ThimbleProjectMigration.js`
    * Used to retrieve the `makeid` for any `ThimbleProject` that has already been published to the **MakeAPI**. This only needs to be run once.
        * `node migrations/ThimbleProjectMakeIDMigration.js` will execute this script, assuming proper `.env` variables have already been setup (instructions above).
        * 
        * 
        * 对Node.js的透视眼镜
这是X射线护目镜的重新启动，以便它充当一个节点的应用程序。

注：本自述假定您已经安装了所有必需的外部依赖，并有一个工作开发环境。新Webmaker？请务必阅读我们的开发者指南，你需要以上手一切！

Prequisites

化妆跟班
迁移

各种脚本都存在，这将有助于在迁移旧数据集以及Node.js的脚本来更新旧记录。

迁移/09052013-附加makeid-column.sql

用于将makeid添加到ThimbleProject数据模型。使用脚本将取决于您的SQL管理环境，但这里的一个命令行提示符下使用它的一个例子：
MySQL的<迁移/09052013-附加makeid-column.sql - 假设你已经做了使用<DB_NAME>
迁移/ ThimbleProjectMigration.js

用于检索makeid对于已被发布到MakeAPI任何ThimbleProject。这仅需要被运行一次。
节点迁移/ ThimbleProjectMakeIDMigration.js将执行这个脚本，假设适当.ENV变量已经被（上述说明）设置。
