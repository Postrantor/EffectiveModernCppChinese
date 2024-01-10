# 《Effective Modern C++ 》翻译

<img src="public/1.png?raw=true" align="right" weight="300" height="400"/>

[![Backers on Open Collective](https://opencollective.com/EffectiveModernCppChinese/backers/badge.svg)](#backers)
[![Sponsors on Open Collective](https://opencollective.com/EffectiveModernCppChinese/sponsors/badge.svg)](#sponsors)

> - 标注“已修订”的章节表示已经没有大致的错误
> - 本书要求读者具有 C++基础
> - [PDF 格式英文版下载](public/EffectiveModernCpp.pdf),仅供翻译参考
> - **[在线浏览(推荐)](https://cntransgroup.github.io/EffectiveModernCppChinese)**

## 目录

0. [**简介**](src/Introduction.md)
1. **类型推导**
   1. [Item 1:理解模板类型推导](src/1.DeducingTypes/item1.md) 已修订
   2. [Item 2:理解 auto 类型推导](src/1.DeducingTypes/item2.md)
   3. [Item 3:理解 decltype](src/1.DeducingTypes/item3.md)
   4. [Item 4:学会查看类型推导结果](src/1.DeducingTypes/item4.md)
2. **auto**
   1. [Item 5:优先考虑 auto 而非显式类型声明](src/2.Auto/item5.md)
   2. [Item 6:auto 推导若非己愿，使用显式类型初始化惯用法](src/2.Auto/item6.md)
3. **移步现代 C++**
   1. [Item 7:区别使用()和{}创建对象](src/3.MovingToModernCpp/item7.md) 已修订
   2. [Item 8:优先考虑 nullptr 而非 0 和 NULL](src/3.MovingToModernCpp/item8.md)
   3. [Item 9:优先考虑别名声明而非 typedefs](src/3.MovingToModernCpp/item9.md)
   4. [Item 10:优先考虑限域枚举而非未限域枚举](src/3.MovingToModernCpp/item10.md) 已修订
   5. [Item 11:优先考虑使用 deleted 函数而非使用未定义的私有声明](src/3.MovingToModernCpp/item11.md)
   6. [Item 12:使用 override 声明重载函数](src/3.MovingToModernCpp/item12.md)
   7. [Item 13:优先考虑 const_iterator 而非 iterator](src/3.MovingToModernCpp/item13.md)
   8. [Item 14:如果函数不抛出异常请使用 noexcept](src/3.MovingToModernCpp/item14.md)
   9. [Item 15:尽可能的使用 constexpr](src/3.MovingToModernCpp/item15.md)
   10. [Item 16:让 const 成员函数线程安全](src/3.MovingToModernCpp/item16.md)
   11. [Item 17:理解特殊成员函数的生成](src/3.MovingToModernCpp/item17.md)
4. **智能指针**
   1. [Item 18:对于独占资源使用 std::unique_ptr](src/4.SmartPointers/item18.md)
   2. [Item 19:对于共享资源使用 std::shared_ptr](src/4.SmartPointers/item19.md) 已修订
   3. [Item 20:当 std::shared_ptr 可能悬空时使用 std::weak_ptr](src/4.SmartPointers/item20.md)
   4. [Item 21:优先考虑使用 std::make_unique 和 std::make_shared，而非直接使用 new](src/4.SmartPointers/item21.md)
   5. [Item 22:当使用 Pimpl 惯用法，请在实现文件中定义特殊成员函数](src/4.SmartPointers/item22.md)
5. **右值引用，移动语义，完美转发**
   1. [Item 23:理解 std::move 和 std::forward](src/5.RRefMovSemPerfForw/item23.md)
   2. [Item 24:区别通用引用和右值引用](src/5.RRefMovSemPerfForw/item24.md)
   3. [Item 25:对于右值引用使用 std::move，对于通用引用使用 std::forward](src/5.RRefMovSemPerfForw/item25.md)
   4. [Item 26:避免重载通用引用](src/5.RRefMovSemPerfForw/item26.md)
   5. [Item 27:熟悉重载通用引用的替代品](src/5.RRefMovSemPerfForw/item27.md)
   6. [Item 28:理解引用折叠](src/5.RRefMovSemPerfForw/item28.md)
   7. [Item 29:认识移动操作的缺点](src/5.RRefMovSemPerfForw/item29.md)
   8. [Item 30:熟悉完美转发失败的情况](src/5.RRefMovSemPerfForw/item30.md)
6. **Lambda 表达式**
   1. [Item 31:避免使用默认捕获模式](src/6.LambdaExpressions/item31.md)
   2. [Item 32:使用初始化捕获来移动对象到闭包中](src/6.LambdaExpressions/item32.md)
   3. [Item 33:对于 std::forward 的 auto&&形参使用 decltype](src/6.LambdaExpressions/item33.md)
   4. [Item 34:优先考虑 lambda 表达式而非 std::bind](src/6.LambdaExpressions/item34.md)
7. **并发 API**
   1. [Item 35:优先考虑基于任务的编程而非基于线程的编程](src/7.TheConcurrencyAPI/Item35.md)
   2. [Item 36:如果有异步的必要请指定 std::launch::async](src/7.TheConcurrencyAPI/item36.md)
   3. [Item 37:从各个方面使得 std::threads unjoinable](src/7.TheConcurrencyAPI/item37.md)
   4. [Item 38:关注不同线程句柄析构行为](src/7.TheConcurrencyAPI/item38.md)
   5. [Item 39:考虑对于单次事件通信使用 void](src/7.TheConcurrencyAPI/item39.md)
   6. [Item 40:对于并发使用 std::atomic，volatile 用于特殊内存区](src/7.TheConcurrencyAPI/item40.md)
8. **微调**
   1. [Item 41:对于那些可移动总是被拷贝的形参使用传值方式](src/8.Tweaks/item41.md)
   2. [Item 42:考虑就地创建而非插入](src/8.Tweaks/item42.md)

## 其他资源

- **[在线阅读(推荐，与翻译内容同步更新)](https://cntransgroup.github.io/EffectiveModernCppChinese)**
- 本书[PDF 格式的中文版](./public/translated/translate-zh-combine.pdf)见于此，该版本通常同步或者滞后于当前 Markdown 文档
- [Effective C++ Xmind Doc](./public/EffectModernC++.xmind)

## 贡献者

感谢所有参与翻译/勘误/建议的贡献者们~
<a href="https://github.com/kelthuzadx/EffectiveModernCppChinese/graphs/contributors"><img src="https://opencollective.com/EffectiveModernCppChinese/contributors.svg?width=890&button=false" /></a>

## 免责声明

译者纯粹出于学习目的与个人兴趣翻译本书，不追求任何经济利益。译者保留对此版本译文的署名权，其他权利以原作者和出版社的主张为准。本译文只供学习研究参考之用，不得公开传播发行或用于商业用途。有能力阅读英文书籍者请购买正版支持。
