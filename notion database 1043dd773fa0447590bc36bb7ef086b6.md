# notion database

# 在 Notion 中使用 JavaScript 插入数据

若想在 Notion 数据库中插入数据，可以通过 JavaScript 代码实现。以下是插入数据的示例代码：

```
const { Client } = require('@notionhq/client');

// 初始化 Notion 客户端
const notion = new Client({ auth: "YOUR_NOTION_API_KEY" });

// 将数据插入 Notion 数据库
async function addToDatabase(name, age, address, price) {
  const response = await notion.pages.create({
    parent: { database_id: "YOUR_DATABASE_ID" },
    properties: {
      Name: { title: [{ text: { content: name } }] },
      Age: { number: age },
      Address: { rich_text: [{ text: { content: address } }] },
      Price: { number: price },
    }
  });
  console.log(response);
}

// 运行代码
addToDatabase("张三", 25, "北京市朝阳区", 10000);

```

需要将 `YOUR_NOTION_API_KEY` 替换为自己的 Notion API Key，将 `YOUR_DATABASE_ID` 替换为自己的 Notion 数据库 ID。此外，代码中的 `name`、`age`、`address` 和 `price` 分别表示要插入的记录的姓名、年龄、地址和价格。

以上代码通过 Notion API 实现了向 Notion 数据库中插入数据的功能，可根据自己的需求进行修改。

你看到的错误提示表明在你的 Notion 数据库中未找到“Name”属性。请确保在数据库中创建了名为“Name”的属性，并将其设置为“Title”类型的属性。您可以在 Notion 中打开数据库，点击右上角的“属性”按钮，并添加一个名为“Name”的新属性，并将其类型设置为“Title”。完成后，请更新代码以引用正确的属性名称，然后再次尝试。

你看到的错误提示表明 `address` 属性的 `id` 没有被定义。在你提供的代码中，`properties` 对象只包含了 `Name`、`Age` 和 `Price` 属性。可能是 `address` 属性还没有被添加到数据库中，或者它的 `id` 已被更改。请检查你的 Notion 数据库，确保 `address` 属性已被添加，并且它的 `id` 是正确的。同时，请确保你已经更新了代码以引用正确的属性ID。

若想通过 JavaScript 代码从 Notion 数据库中删除记录，可以使用以下示例代码：

```
const { Client } = require('@notionhq/client');

// 初始化 Notion 客户端
const notion = new Client({ auth: "YOUR_NOTION_API_KEY" });

// 从 Notion 数据库中删除记录
async function deleteFromDatabase(recordId) {
  const response = await notion.pages.update({
    page_id: recordId,
    properties: {
      "已归档": { checkbox: true }
    }
  });
  console.log(response);
}

// 运行代码
deleteFromDatabase("RECORD_ID_TO_DELETE");

```

需要将 `YOUR_NOTION_API_KEY` 替换为自己的 Notion API Key，将 `RECORD_ID_TO_DELETE` 替换为要删除的记录的 ID。此外，代码中的 `已归档` 表示一个名为“已归档”的属性，它是一个复选框类型的属性，用于标记要删除的记录。你可以根据自己的需求修改这个属性的名称和类型。

以上代码通过 Notion API 实现了从 Notion 数据库中删除记录的功能，可根据自己的需求进行修改。

你看到的错误提示表明数据库中不存在名为“已归档”的属性。请确保在数据库中创建了名为“已归档”的属性，并将其设置为“Checkbox”类型的属性。您可以在 Notion 中打开数据库，点击右上角的“属性”按钮，并添加一个名为“已归档”的新属性，并将其类型设置为“Checkbox”。完成后，请更新代码以引用正确的属性名称，然后再次尝试。

如果你看到的错误提示是 `name`、`age` 或 `price` 属性未定义，那么可能是因为你没有正确定义这些属性。请确保在 Notion 数据库中创建了这些属性，并将它们设置为正确的属性类型。

另外，如果你看到的错误提示是 `database_id` 未定义，那么可能是因为你没有正确设置 `parent` 属性。请确保在代码中正确设置了 `parent` 属性，并将其设置为你的数据库 ID。

以上是常见错误的解决方案，你可以根据你的实际情况进行相应的修改。如果你还有其他问题，可以在 Notion 官方文档中查找相关的 API 文档，或者在社区中寻求帮助。

若想通过 JavaScript 代码从 Notion 数据库中根据 ID 查询一条记录，可以使用以下示例代码：

```
const { Client } = require('@notionhq/client');

// 初始化 Notion 客户端
const notion = new Client({ auth: "YOUR_NOTION_API_KEY" });

// 从 Notion 数据库中根据 ID 查询一条记录
async function getRecordById(recordId) {
  const response = await notion.pages.retrieve({ page_id: recordId });
  console.log(response);
}

// 运行代码
getRecordById("RECORD_ID_TO_RETRIEVE");

```

需要将 `YOUR_NOTION_API_KEY` 替换为自己的 Notion API Key，将 `RECORD_ID_TO_RETRIEVE` 替换为要查询的记录的 ID。

以上代码通过 Notion API 实现了从 Notion 数据库中根据 ID 查询一条记录的功能，可根据自己的需求进行修改。

请注意，以上代码仅能查询单个记录，如果想要查询多个记录，则需要使用 Notion 的查询功能。你可以在 Notion 官方文档中查找相关的 API 文档，或者在社区中寻求帮助。