# phpinifile
PHP实现ini文件操作类
# 操作方法
实例化ini文件操作类，并载入 .ini文件

$iniFile = new iniFile('./config.ini');

添加一个分类

$iniFile->addCategory('config');

添加一个分类并直接添加子项

$iniFile->addCategory('config', ['test1' => 123, 'test2' => 456]);

添加一个子项(如果子项存在，则覆盖;)

$iniFile->addItem('config',['test1' => 123]);

删除一个分类

$iniFile->delCategory('config');

删除一个子项

$iniFile->delItem('config', 'test1');

修改一个分类下子项的值(也可以修改多个)

$iniFile->updItem('config', ['test1' => 789]);

获取一个分类下所有数据

print_r($iniFile->getCategory('config'));

获取一个分类下某个子项的值

print_r($iniFile->getItem('config','test1'));

获取一个分类下多个子项的值

print_r($iniFile->getItem('config',['test1', 'test2']));

获取ini文件中所有分类及子项

print_r($iniFile->getAll());

或者

print_r($iniFile->iniFileHandle);
