# Lego注册器

_Code: `Lego/LegoRegister.php`_


## 添加注册项

在 `Lego/Register` 中创建对应数据类，示例如下：

```php
class FieldData extends Data
{
    /**
     * 校验注册的数据是否合法, 不合法时抛出异常
     * @param $data
     */
    protected function validate($data)
    {
    }

    /**
     * 注册完成后的回调 （可选）
     */
    public function afterRegistered()
    {
    }
    
    // other helper methods
}

```


## 注册

```php

lego_register(FieldData::class, [
	'address' => ['description' => '地址'],
	// ..
], Room::class);
```


## 使用注册的数据

```php

$data = Register::get(FieldData::class, Room::class);
```
