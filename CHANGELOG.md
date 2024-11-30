# Changelog

## [1.6.2](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.6.1...v1.6.2) (2024-11-30)


### Documentation

* **README:** updated requirements ([5dff82c](https://github.com/antmelekhin/ansible-role-containerd/commit/5dff82c2929200e42d4d35001ad01b062a75b8f4))


### Styles

* updated jinja templates ([5eb13dd](https://github.com/antmelekhin/ansible-role-containerd/commit/5eb13dd4fe016c75e924d71b4952e2a0c3e7163c))

## [1.6.1](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.6.0...v1.6.1) (2024-10-30)


### Code Refactoring

* update `vars/main.yml` file ([f0f7206](https://github.com/antmelekhin/ansible-role-containerd/commit/f0f72066e544bb81aac7066554cc8ed7564173bf))


### Continuous Integration

* use `ubuntu-22.04` instead of `ubuntu-latest` ([0bc5543](https://github.com/antmelekhin/ansible-role-containerd/commit/0bc55434cae6026dc3834bc2e6f655983f6babd3))


### Styles

* minor fixes ([5660c89](https://github.com/antmelekhin/ansible-role-containerd/commit/5660c89bd0ae3e9c822f25e11cccad79b9876d7d))

## [1.6.0](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.5.0...v1.6.0) (2024-08-11)


### Improvements

* merge OS-specific variables into the `vars/main.yml` file ([#7](https://github.com/antmelekhin/ansible-role-containerd/issues/7)) ([d948302](https://github.com/antmelekhin/ansible-role-containerd/commit/d9483026b243a1fcad326452fb76ca5c1d4e074c))

## [1.5.0](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.4.0...v1.5.0) (2024-08-03)


### Improvements

* update vars ([#6](https://github.com/antmelekhin/ansible-role-containerd/issues/6)) ([aa98ce5](https://github.com/antmelekhin/ansible-role-containerd/commit/aa98ce53311bf2aca7054d6c00036ffc754da29e))

## [1.4.0](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.3.0...v1.4.0) (2024-07-22)


### Features

* add `meta/argument_specs.yml` ([#5](https://github.com/antmelekhin/ansible-role-containerd/issues/5)) ([4d2a3aa](https://github.com/antmelekhin/ansible-role-containerd/commit/4d2a3aa4d060a425ad28e90797c92f084e2bc9e2))

## [1.3.0](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.2.1...v1.3.0) (2024-07-22)


### Features

* add fedora support ([6e43e0e](https://github.com/antmelekhin/ansible-role-containerd/commit/6e43e0ef4e4ca906673fafb41976a14bb324960f))


### Styles

* update common role style ([#4](https://github.com/antmelekhin/ansible-role-containerd/issues/4)) ([9550fc4](https://github.com/antmelekhin/ansible-role-containerd/commit/9550fc45b28b6bbbae16450f3f340353e3088ff1))

## [1.2.1](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.2.0...v1.2.1) (2024-05-13)


### Documentation

* **README:** update variables documentation ([c96c5c1](https://github.com/antmelekhin/ansible-role-containerd/commit/c96c5c1fe23e6ffad02539e0903ca37859636e3e))


### Styles

* rename tasks ([57ff371](https://github.com/antmelekhin/ansible-role-containerd/commit/57ff37179bcb08605aa850bc37bfb06d054d2280))

## [1.2.0](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.1.0...v1.2.0) (2024-05-08)


### Features

* add `containerd_registries_auth` variable ([beb7d34](https://github.com/antmelekhin/ansible-role-containerd/commit/beb7d347c5894ca17f14f963f4609e3847fa1faa))

## [1.1.0](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.0.3...v1.1.0) (2024-05-02)


### Features

* add `config.toml.j2` ([#1](https://github.com/antmelekhin/ansible-role-containerd/issues/1)) ([1255bef](https://github.com/antmelekhin/ansible-role-containerd/commit/1255bef409c6ba896693b2a3e8f4f9fd2f36c36f))


### Styles

* add newline to end of file ([8b0eea8](https://github.com/antmelekhin/ansible-role-containerd/commit/8b0eea8731e64d69a2f28c76a6503fa64bd2d84c))

## [1.0.3](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.0.2...v1.0.3) (2024-04-25)


### Documentation

* **README:** fixed examples view ([4d6153d](https://github.com/antmelekhin/ansible-role-containerd/commit/4d6153dfc9625dccb9d7960877588e5795e35773))


### Fixes

* fixed running a role in `check_mode` ([b6280dd](https://github.com/antmelekhin/ansible-role-containerd/commit/b6280ddb22aa357e6ed5674ac278ebada0be0665))

## [1.0.2](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.0.1...v1.0.2) (2024-04-24)


### Fixes

* **test:** run linters in its own workflow ([#3](https://github.com/antmelekhin/ansible-role-containerd/issues/3)) ([9204ced](https://github.com/antmelekhin/ansible-role-containerd/commit/9204ced419366313fd7480d906110ce07fb3fedc))

## [1.0.1](https://github.com/antmelekhin/ansible-role-containerd/compare/v1.0.0...v1.0.1) (2024-04-20)


### Code Refactoring

* update variable names, rm conditional expression, quote strings and rm loop for `include_vars` ([#2](https://github.com/antmelekhin/ansible-role-containerd/issues/2)) ([57c1ba8](https://github.com/antmelekhin/ansible-role-containerd/commit/57c1ba8a400fc66ea160faae1b6b37c42eaf6507))


### Continuous Integration

* update release rules ([02a507d](https://github.com/antmelekhin/ansible-role-containerd/commit/02a507d648b024e16df44451b8663f66cf8851c3))
* update workflows ([3e7991f](https://github.com/antmelekhin/ansible-role-containerd/commit/3e7991f70ecd687340635c94174813174afcb485))

## [1.0.0](https://github.com/antmelekhin/ansible-role-containerd/compare/...v1.0.0) (2024-03-05)


### Features

* initial commit ([a87ae65](https://github.com/antmelekhin/ansible-role-containerd/commit/a87ae65d405fd3c5c670187ca574d38f1b43a2ce))
