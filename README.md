# AngularBase

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 15.2.2.

## Build và commit code

- > Chạy lệnh: npm install để fetch node_modules.
- > Chạy lệnh: npm start để chạy chương trình
- > Mỗi người sẽ có 1 branch riêng để lập trình.
- > Mỗi lần trước khi commit sẽ thực hiện pull code từ branch develop về, tiến hành merge rồi commit code lên branch của mình và branch develop, code build lên môi trường test sẽ từ branch develop.

## Quy tắc đặt tên

- Tên Class viết theo kiểu: Pascal Case (ThisWordIsInPascalCase) ví dụ: export class ConfigurationClass
- Tên Hàm viết theo kiểu: Camel Case (thisWordIsInPascalCase) ví dụ: configurationFunction(){}
- Tên "export const ..." viết theo kiểu Camel Case (thisWordIsInCamelCase) ví dụ: export const configurationRouter

## Đặt tên trong file đa ngôn ngữ

- `src\assets\i18n\vi-VN.json`
- Quy ước chung đặt label cho các chức năng riêng
- Tên module (catalog, product…. )
- Tên chức năng (stock-warehouse, routing)
- Tên thành phần trên màn hình (label, button, grid…)
- Các thành phần phụ nếu có sẽ được thêm vào phía sau (có thể thêm đuôi nếu cần thiết)
  Ví dụ: catalog.stock-warehouse.label.add: "Thêm mới", catalog.stock-warehouse.button.delete: "Xóa",

  ## Một số lưu ý chung

- Các control, message, label trên màn hình đều phải sử dụng đa ngôn ngữ
  - Với code html: {{ 'menu.account.logout' | translate}}
  - Để thay đổi ngôn ngữ vào **app.component.ts** thay đổi **defaultLanguage**,

-Comment trên mỗi hàm khai báo nên sử dụng kiểu <strong>/\*\* \*/</strong>
Ví dụ:

```
/**
Hàm testFunction làm.....
*/
testFunction(){}
```

- Các api chỉ trả ra dữ liệu cần thiết, hạn chế trả ra dữ liệu thừa - performance kém
  - Table dùng api riêng
  - List của combo box sẽ dùng api riêng

## Cấu trúc thư mục

```
├── src
│   ├── app
│   │   ├── auth
│   │   │   └── auth.module.ts                  # Auth module
│   │   ├── core
│   │   │   └── core.module.ts                  # Core module
│   │   ├── layout                              # Layout
│   │   │   └── layout.module.ts
│   │   ├── pages                               # Pages
│   │   │   ├── pages.module.ts
│   │   │   └── pages-routing.module.ts
│   │   ├── services                            # Services
│   │   ├── shared                              # Shared
│   │   │   └── shared.module.ts
│   │   ├── app.component.ts                    # Root component
│   │   └── app.module.ts                       # Root module
│   ├── assets                                  # Local static files
│   │   │── i18n                                # Language folder
│   ├── environments                            # Environment configuration
│   ├── styles                                  # Project styles
└── └── style.less                              # Style entry
```
