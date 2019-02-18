
/** 文件说明
  * 标有 ✅ 的规则视为错误，禁止出现
  * 标有 🔨 的规则表示可以通过 --fix 自动修复
  * 未标状态的视为当前阶段非必须遵守的
  * LintType 值与构建环境相关
  */
let LintType = process.env.NODE_ENV === "production" ? "error" : "off"

module.exports = {
    root: true,
    parser: 'babel-eslint',
    env: {
        browser: true,
        commonjs: true,
        es6: true,
        jest: true
    },
    extends: [
        "eslint:recommended",  /**✅ eslint官方推荐*/
        "plugin:react/recommended" /**✅ react官方推荐*/
    ],
    globals: {
        process: {
            env: {
                NODE_ENV: process.env.NODE_ENV
            }
        }
    },
    parserOptions: {
        ecmaFeatures: {
            jsx: true,
            classes: true
        },
        ecmaVersion: 2018,
        sourceType: "module"
    },
    plugins: [
        "react"
    ],
    rules: {
        //✅ 🔨 缩进方式，用 4 个空格缩进, 请在提交前注释 indent ， eslint 似乎有bug
        // indent: ["error", 4, {
        //     SwitchCase: 1
        // }],
        //✅ 禁止使用tab缩进
        "no-tabs": "error",
        //✅ 换行符样式
        "linebreak-style": ["error", "unix"],
        //🔨 使用双引号
        // quotes: ["error", "double"],
        //🔨 不需要末尾的 ;
        // semi: ["error", "never"],
        //✅ 强制使用 === 和 !==
        eqeqeq: "error",
        //✅ 要求构造函数首字母大写
        "new-cap": LintType,
        //✅ 要求调用无参构造函数时有圆括号
        "new-parens": "error",
        //✅ 禁止使用eval
        "no-eval": "error",
        //强制有效的 jsdoc 注释
        // "require-jsdoc": [
        //     "error",
        //     {
        //         require: {
        //             FunctionDeclaration: true,
        //             MethodDefinition: false,
        //             ClassDeclaration: true,
        //             ArrowFunctionExpression: false,
        //             FunctionExpression: false
        //         }
        //     }
        // ],
        // "valid-jsdoc": "error",
        //✅ generator 函数需要 yield
        "require-yield": "error",
        //✅ async 函数需要 yield
        "require-await": "error",
        //✅ 🔨 不使用var定义变量
        "no-var": "error",
        //✅ 禁止在注释中使用特定的警告术语 todo , fixme
        "no-warning-comments": LintType,
        //🔨 文件末尾需要一个空行
        // "eol-last": [LintType, "always"],
        //禁止出现空函数
        // "no-empty-function": "error",
        //🔨 禁止使用多个空格
        // "no-multi-spaces": "error",
        //✅ 禁用 with
        "no-with": "error",
        //✅ 🔨 要求或禁止 “Yoda” 条件
        yoda: "error",
        //✅ 禁止 this 关键字出现在类和类对象之外
        // "no-invalid-this": "error",
        // 禁止在常规字符串中出现模板字面量占位符语法
        // "no-template-curly-in-string": "error",
        //🔨 禁止冗余的括号
        // "no-extra-parens": "error",
        //🔨 要求 IIFE 使用括号括起来
        // "wrap-iife": "error",
        //🔨 禁止初始化为 undefined
        // "no-undef-init": "error",
        //✅ 禁止将 undefined 作为标识符
        "no-undefined": "error",
        //✅ 禁用未定义的变量
        "no-undef": "error",
        // 链式调用独占一行
        // "newline-per-chained-call": LintType,
        // 警告多余的空行
        // "no-multiple-empty-lines": "warn",
        //✅ 禁止使用 url 脚本
        "no-script-url": "error",
        //✅ 禁用自身比较
        "no-self-compare": "error",
        //✅ 禁止一层比变的循环条件
        "no-unmodified-loop-condition": "error",
        //✅ 禁止操作__proto__
        "no-proto": "error",
        //禁止用 new 调用Function
        // "no-new-func": "error",
        //数组方法必须有返回值
        // "array-callback-return": "error",
        // "max-len": [
        //   LintType,
        //   {
        //     code: 120,
        //     tabWidth: 4,
        //     ignoreUrls: true,
        //     ignoreTemplateLiterals: true
        //   }
        // ],
        //🔨 尽量使用 const
        // "prefer-const": "error",
        //🔨 尽量使用 spread
        // "prefer-spread": "error",
        // 禁用 alert 和 console -- production 环境下是错误 , development 环境下是警告
        "no-alert": LintType,
        "no-console": LintType,

        //react
        //props 的布尔值属性需要以 is 或 has 开头
        // "react/boolean-prop-naming": [
        //   "error",
        //   { rule: "^(is|has)[A-Z]([A-Za-z0-9]?)+" }
        // ],
        //✅ 非 require 的属性,必须有默认值
        // "react/require-default-props": [
        //     "error",
        //     { forbidDefaultForRequired: true }
        // ],
        // "react/default-props-match-prop-types": [
        //   "error",
        //   { allowRequiredDefaults: true }
        // ],
        //🔨 boolean 属性值为 true 时不需要写值
        // "react/jsx-boolean-value": ["error", "never"],
        //✅ 必须添加 key 属性
        "react/jsx-key": "error",
        //✅ 禁用重复属性
        "react/jsx-no-duplicate-props": "error",
        //✅ 禁用 setinnerHTMl
        "react/no-danger-with-children": "error",
        "react/no-danger": "error",
        //禁止在特定的生命周期中使用 setstate
        // "react/no-did-mount-set-state": "error",
        // "react/no-did-update-set-state": "error",
        //✅ 禁止直接设置 state
        "react/no-direct-mutation-state": "error",
        //禁用 ReactDOM.render 的返回值
        // "react/no-render-return-value": "error",
        //禁用字符串的 ref
        // "react/no-string-refs": "error",
        //强制使用 stateless component
        // "react/prefer-stateless-function": "error",
        //render 函数需要返回值
        // "react/require-render-return": "error",
        //✅ 🔨 对 prop-types 排序
        "react/sort-prop-types": "warn",
        //✅ 🔨 对组件方法排序
        "react/sort-comp": "warn",
        //强制 style prop 是一个 object
        // "react/style-prop-object": "error",
        //禁止给无子元素标签添加子元素
        // "react/void-dom-elements-no-children": "error",
        "react/no-find-dom-node": LintType
    }
}
