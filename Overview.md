# 概览

Passport 是一个 Node 平台的身份认证中间件。它的设计服务于一个简单的目标：身份认证请求。编写模块时，封装是一个美德，所以 Passport 把所有其他功能交给应用自身去做。这种关注点的分离可以保持代码整洁并且可维护，同时使得 Passport 极其容易地集成到应用中。

在现代 web 应用中，身份认证可以采用多种形式。传统而言，用户通过提供用户名和密码登录。由于社交网络的兴起，使用类似于 Facebook 或者 Twitter 的 OAuth 提供商进行单点登录（single sign-on）已经成为一个流行的身份验证方式。暴露 API 的服务通常需要基于 token 的凭证来保护访问行为。

Passport 认为每一个应用都有独一无二的身份认证需求。身份认证机制，被称为策略(strategies)，打包成独立的模块。应用可以选择应用哪些策略，同时避免创建不必要的依赖。

尽管身份验证过程很复杂，代码也可以很简洁。

```javascript
app.post('/login', passport.authenticate('local', { successRedirect: '/',
                                                    failureRedirect: '/login' }));
```

## Install

```shell
$ npm install passport
```

> Original: http://www.passportjs.org/docs/