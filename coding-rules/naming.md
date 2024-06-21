## SUHE代码命名规范

> 包括但不限于React TypeScript相关项目实践

1. 文件命名:
   - 使用小写字母
   - 多个单词用连字符(-)分隔，如 `user-profile.ts`
   - React组件文件使用PascalCase，如 `UserProfile.tsx`
   - 测试文件添加 `.test.ts` 或 `.spec.ts` 后缀
   - 样式文件使用 `.module.css` 后缀表示CSS模块

2. 组件命名:
   - 使用PascalCase，如 `UserProfile`
   - 高阶组件可以使用 `with` 前缀，如 `withAuth`

3. Hook命名:
   - 使用 `use` 前缀，如 `useLocalStorage`

4. 类型和接口:
   - 使用PascalCase
   - 接口不要加 `I` 前缀
   - 类型可以使用 `Type` 后缀，如 `UserType`

5. 常量:
   - 使用全大写，下划线分隔，如 `MAX_COUNT`

6. 函数和变量:
   - 使用camelCase
   - 布尔值可以使用 `is`、`has`、`can` 等前缀

7. 事件处理函数:
   - 使用 `handle` 前缀，如 `handleClick`

8. Props:
   - 使用camelCase
   - 避免使用缩写

9. 枚举:
   - 枚举名使用PascalCase
   - 枚举成员使用PascalCase

10. 命名空间:
    - 使用PascalCase

遵循这些命名规范可以提高代码的一致性和可读性。团队应该根据具体项目需求制定详细的命名规范文档，并在代码审查中严格执行。

## 补充：文件夹命名

1. 主要文件夹:
   - 使用小写字母
   - 单个单词优先，如 `components`, `pages`, `hooks`, `utils`
   - 如果需要多个单词，使用kebab-case（短横线连接），如 `api-services`

2. 组件文件夹:
   - 使用PascalCase，与组件名称一致
   - 例如: `Button`, `UserProfile`, `NavigationBar`

3. 特性或模块文件夹:
   - 使用小写字母
   - 如果是多个单词，使用kebab-case
   - 例如: `user-management`, `product-catalog`

4. 版本文件夹:
   - 如果需要版本控制，使用 `v` 前缀加数字
   - 例如: `v1`, `v2`

5. 测试文件夹:
   - 使用小写的 `__tests__`

6. 类型定义文件夹:
   - 使用小写的 `types` 或 `interfaces`

7. 资源文件夹:
   - 使用小写，如 `assets`, `images`, `fonts`

8. 环境配置文件夹:
   - 使用小写，如 `config`, `environments`

9. 布局组件文件夹:
   - 使用小写的 `layouts`

10. 公共组件文件夹:
    - 使用小写的 `common` 或 `shared`

示例文件结构：

```
src/
  components/
    Button/
    UserProfile/
    NavigationBar/
  pages/
  hooks/
  utils/
  api-services/
  assets/
    images/
    fonts/
  types/
  layouts/
  common/
  features/
    user-management/
    product-catalog/
  __tests__/
  config/
```

这种命名方式有助于保持项目结构的一致性和清晰度。记住，最重要的是在团队内部达成共识，并在整个项目中保持一致。可以将这些规范写入团队的开发文档中，确保所有成员都遵循相同的命名约定。

## 单复数名词规范

1. 文件夹命名：
   - 通常使用单数形式，如 `component`, `util`, `hook`
   - 表示集合的文件夹可以使用复数，如 `pages`, `styles`

2. 文件命名：
   - 组件文件使用单数，如 `Button.tsx`, `UserProfile.tsx`
   - 工具函数文件通常用单数，如 `format.ts`, `validate.ts`
   - 类型定义文件可以用复数，如 `types.ts`, `interfaces.ts`

3. 变量命名：
   - 单个实例用单数，如 `const user = {...}`
   - 表示多个项目的数组或集合用复数，如 `const users = [...]`

4. 接口和类型命名：
   - 通常使用单数，如 `interface User`, `type ButtonProps`

5. 组件Props命名：
   - 单个项目用单数，如 `user: User`
   - 多个项目的数组用复数，如 `users: User[]`

6. 函数命名：
   - 处理单个项目的函数用单数，如 `getUser()`
   - 处理多个项目的函数用复数，如 `fetchUsers()`

7. Hook命名：
   - 通常使用单数，如 `useUser`, `useForm`

8. 上下文（Context）命名：
   - 通常使用单数，如 `UserContext`, `ThemeContext`

9. 常量命名：
   - 单个值用单数，如 `const MAX_COUNT = 10`
   - 多个值的数组用复数，如 `const ALLOWED_SIZES = ['small', 'medium', 'large']`

10. Redux相关命名：
    - Action类型通常用单数，如 `USER_LOGIN`
    - Reducer通常用单数，如 `userReducer`
    - Selector通常根据返回值决定，如 `selectUser`, `selectAllUsers`

总的来说，命名应该清晰地表达其内容和用途。使用单数还是复数应该基于它代表的是单个实体还是多个实体的集合。保持一致性是关键，一旦在项目中采用了某种约定，就应该在整个项目中保持一致。

## 组合短语及前后顺序

根据常见的React和TypeScript项目实践，以下是关于使用动词、形容词、副词和名词等组成短语来命名各种元素时的规范建议：

1. 变量命名：
   - 使用名词或名词短语
   - 形容词+名词：`const activeUser = ...`
   - 动词过去分词+名词：`const selectedItems = ...`

2. 文件命名：
   - 组件文件：使用名词或名词短语，PascalCase，如 `UserProfile.tsx`
   - 工具文件：使用名词，camelCase，如 `stringUtils.ts`

3. 组件命名：
   - 使用名词或名词短语，PascalCase
   - 形容词+名词：`ActiveUserList`
   - 动词过去分词+名词：`EnhancedTable`

4. 常量命名：
   - 使用名词或名词短语，全大写，下划线分隔
   - 形容词+名词：`MAX_USER_COUNT`
   - 动词过去分词+名词：`ALLOWED_FILE_TYPES`

5. 函数命名：
   - 使用动词或动词短语，camelCase
   - 动词+名词：`getUserData()`
   - 动词+形容词+名词：`fetchActiveUsers()`
   - 情态动词（can/is/has）+动词/形容词：`canEdit()`, `isValid()`, `hasPermission()`

6. 布尔值变量或属性：
   - 使用 is/has/can 等前缀：`isActive`, `hasChildren`, `canEdit`

7. 事件处理函数：
   - 使用 handle 前缀：`handleClick`, `handleInputChange`

8. 异步函数：
   - 可以使用 async 前缀：`asyncFetchData`

9. Getter函数：
   - 使用 get 前缀：`getUserName()`

10. Setter函数：
    - 使用 set 前缀：`setUserName()`

11. 工厂函数：
    - 使用 create 前缀：`createUser()`

12. 转换函数：
    - 使用 to 前缀：`toUpperCase()`, `toString()`

13. 计算属性或方法：
    - 使用形容词或名词：`fullName`, `totalPrice`

时态方面：
- 一般使用现在时
- 对于表示状态的变量，可以使用过去分词：`isLoaded`, `isCompleted`

前后位置：
- 形容词通常放在名词前面：`smallSize`, `redButton`
- 动词（在函数名中）通常放在最前面：`getData()`, `updateUser()`

记住，最重要的是在项目中保持一致性。这些规则可以根据团队的偏好和项目的具体需求进行调整。将这些规范写入团队的开发文档中，并在代码审查过程中严格执行，可以帮助维护代码的清晰度和一致性。

Citations:
[1] https://www.linkedin.com/pulse/best-practices-rule-example-20-clean-code-react-js-coding
[2] https://xieqingtian.github.io/2019/01/28/react%E5%92%8Ctypescript%E9%A1%B9%E7%9B%AE%E5%BC%80%E5%8F%91%E8%A7%84%E8%8C%83/
[3] https://dev.to/sathishskdev/part-1-naming-conventions-the-foundation-of-clean-code-51ng
[4] https://www.linkedin.com/pulse/react-js-naming-convention-kristiyan-velkov
[5] https://juejin.cn/post/6844904098106441741