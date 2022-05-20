---
nav:
  title: Components
  path: /components

group:
  title: MyModal
---
## MyModal

| Name | Description | Type    | Default |
|------|-------------|---------|---------|
| isMy | 自定义属性  | boolean | -       |
| ...  | ...         | ...     | ...     |

```tsx
/**
 * title: 我是标题
 * desc: 我是简介，我可以用 `Markdown` 来编写
 * background: 'red'
 */
import React,{ useState } from 'react';
import {  MyButton, MyModal } from 'my-dumi-doc';

const MyModalDemo = () => {
  const [isModalVisible, setIsModalVisible] = useState(false);

  const showModal = () => {
    setIsModalVisible(true);
  };

  const handleOk = () => {
    setIsModalVisible(false);
  };

  const handleCancel = () => {
    setIsModalVisible(false);
  };

  return (
    <>
      <MyButton type="primary" onClick={showModal}>
        Open Modal
      </MyButton>
      <MyModal title="Basic Modal" visible={isModalVisible} onOk={handleOk} onCancel={handleCancel}>
        <p>Some contents...</p>
        <p>Some contents...</p>
        <p>Some contents...</p>
      </MyModal>
    </>
  );
};

export default () => <MyModalDemo />;
```
<API></API>
