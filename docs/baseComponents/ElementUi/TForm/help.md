# TForm 参数配置

### 1. 简介：基于 ElementUI Form 表单组件的二次封装，着重于数据层面，HTML 一行代码

TForm 表单组件
**代码示例：**

```html
<t-form
  :ref-obj.sync="formOpts.ref"
  :formOpts="formOpts"
  :widthSize="1"
  @handleEvent="handleEvent"
/>
//注意:ref-obj(form校验规则相当于ref)必须要‘.sync’修饰符
```

### 2. events

| 事件名      | 说明                 | 返回值                                                   |
| :---------- | :------------------- | :------------------------------------------------------- |
| handleEvent | 单个查询条件触发事件 | fieldList 中 type/查询条件输入的值/fieldList 中 event 值 |

### 3. Methods

| 事件名        | 说明     | 参数 |
| :------------ | :------- | :--- |
| resetFields   | 重置表单 | -    |
| clearValidate | 清空校验 | -    |

### 4. 配置参数

| 参数                | 说明                                                                                                    | 类型         | 默认值      |
| :------------------ | :------------------------------------------------------------------------------------------------------ | :----------- | :---------- |
| refObj              | form 表单校验规则方法 （可以参考 elementUI Form 表单方法中的 validate）                                 | obj          | -           |
| className           | 自定义类名                                                                                              | String       | -           |
| labelPosition       | 改变表单项 label 与输入框的布局方式(默认：right) /top                                                   | String       | 'right'     |
| widthSize           | 每行显示几个输入项（默认两项） 最大值 4                                                                 | Number       | 2           |
| formOpts            | 表单配置项                                                                                              | Object       | {}          |
| ---listTypeInfo     | 下拉选择数据源（type:'select'有效）                                                                     | Object       | {}          |
| ---fieldList        | form 表单每项 list                                                                                      | Array        | []          |
| ------isHideItem    | 某一项不显示                                                                                            | Boolean      | false       |
| ------slotName      | 自定义表单某一项输入框                                                                                  | slot         | -           |
| ------childSlotName | 自定义表单某一下拉选择项子组件插槽（el-option）                                                         | slot         | -           |
| ------comp          | form 表单每一项组件是输入框还是下拉选择等（可使用第三方 UI 如 el-select/el-input 也可以使用自定义组件） | String       | -           |
| ------bind          | 表单每一项属性（继承第三方 UI 的 Attributes，如 el-input 中的 clearable 清空功能）默认清空及下拉过滤    | Object       | {}          |
| ------type          | form 表单每一项类型                                                                                     | String       | 是          |
| ------widthSize     | form 表单某一项所占比例(如果占一整行则设置 1)                                                           | Number       | 2           |
| ------width         | form 表单某一项所占实际宽度                                                                             | String       | 100%        |
| ------arrLabel      | type=select-arr 时，每个下拉显示的中文                                                                  | String       | 'dictLabel' |
| ------arrKey        | type=select-arr 时，每个下拉显示的中文传后台的数字                                                      | String       | 'dictValue' |
| ------label         | form 表单每一项 title                                                                                   | String       | -           |
| ------labelRender   | 自定义某一项 title                                                                                      | function     | -           |
| ------value         | form 表单每一项传给后台的参数                                                                           | String       | -           |
| ------rules         | 每一项输入框的表单校验规则                                                                              | Object/Array | -           |
| ------list          | 下拉选择数据源（仅仅对 type:'select'有效）                                                              | String       | -           |
| ------event         | 表单每一项事件标志（handleEvent 事件）                                                                  | String       | -           |
| ---formData         | 表单提交数据(对应 fieldList 每一项的 value 值)                                                          | Object       | -           |
| ---labelWidth       | label 宽度                                                                                              | String       | 120px       |
| ---rules            | 规则（可依据 elementUI el-form 配置————对应 formData 的值）                                             | Object/Array | -           |
| ---operatorList     | 操作按钮 list                                                                                           | Array        | -           |

### 5. 关于 element-ui el-form/el-form-item 提供的一些方法/属性可直接使用，无需其他配置
