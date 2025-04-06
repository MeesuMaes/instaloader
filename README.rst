.. image:: https://raw.githubusercontent.com/instaloader/instaloader/master/docs/logo_heading.png

.. badges-start

|pypi| |pyversion| |license| |aur| |contributors| |downloads|

.. |pypi| image:: https://img.shields.io/pypi/v/instaloader.svg
   :alt: Instaloader PyPI 项目页面
   :target: https://pypi.org/project/instaloader/

.. |license| image:: https://img.shields.io/github/license/instaloader/instaloader.svg
   :alt: MIT 许可证
   :target: https://github.com/instaloader/instaloader/blob/master/LICENSE

.. |pyversion| image:: https://img.shields.io/pypi/pyversions/instaloader.svg
   :alt: 支持的 Python 版本

.. |contributors| image:: https://img.shields.io/github/contributors/instaloader/instaloader.svg
   :alt: 贡献者数量
   :target: https://github.com/instaloader/instaloader/graphs/contributors

.. |aur| image:: https://img.shields.io/aur/version/instaloader.svg
   :alt: Arch 用户存储库包
   :target: https://aur.archlinux.org/packages/instaloader/

.. |downloads| image:: https://pepy.tech/badge/instaloader/month
   :alt: PyPI 下载量
   :target: https://pepy.tech/project/instaloader

.. badges-end

::

    $ pip3 install instaloader

    $ instaloader profile [profile ...]

**Instaloader**

- 下载**公共和私人个人资料、标签、用户故事、动态和保存的媒体**，

- 下载每篇帖子的**评论、地理标签和说明文字**，

- 自动**检测个人资料名称更改**并相应地重命名目标目录，

- 允许对过滤器和存储下载媒体的位置进行**精细定制**，

- 自动**恢复之前中断的**下载迭代。

::

    instaloader [--comments] [--geotags]
                [--stories] [--highlights] [--tagged] [--reels] [--igtv]
                [--login 您的用户名] [--fast-update]
                profile | "#标签" | :stories | :feed | :saved

`Instaloader 文档 <https://instaloader.github.io/>`__


如何自动从 Instagram 下载图片
-----------------------------------------------------

要**下载某个个人资料的所有图片和视频**，以及**个人资料图片**，请执行以下操作：

::

    instaloader profile [profile ...]

其中 ``profile`` 是您想要下载的个人资料名称。您也可以指定多个个人资料的列表，而不仅仅是一个。

要稍后**更新您本地的个人资料副本**，您可以运行：

::

    instaloader --fast-update profile [profile ...]

如果使用了 ``--fast-update``，Instaloader 会在到达第一个已下载的图片时停止。

或者，您可以使用 ``--latest-stamps`` 让 Instaloader 存储每个个人资料最后一次下载的时间，并只下载更新的媒体：

::

    instaloader --latest-stamps -- profile [profile ...]

使用此选项，即使移动或删除了已下载的媒体，仍然可以保持存档的更新。

更新个人资料时，Instaloader 会自动**检测个人资料名称更改**并相应地重命名目标目录。

Instaloader 还可以用于**下载私人个人资料**。为此，请使用以下命令：

::

    instaloader --login=您的用户名 profile [profile ...]

登录时，Instaloader 会将**会话 cookie 存储**在您的临时目录中的一个文件中，下次使用 ``--login`` 时会重用该文件。因此，当您已经拥有有效的会话 cookie 文件时，可以**非交互式**下载私人个人资料。

`Instaloader 文档 <https://instaloader.github.io/basic-usage.html>`__

贡献
------------

作为一个开源项目，Instaloader 在很大程度上依赖于其社区的贡献。查看
`贡献指南 <https://instaloader.github.io/contributing.html>`__
了解您如何帮助 Instaloader 成为一个更强大的工具。

支持者
----------

.. current-sponsors-start

| Instaloader 由以下赞助商自豪支持：
|  `@rocketapi-io <https://github.com/rocketapi-io>`__

请访问 `Alex 的 GitHub 赞助页面 <https://github.com/sponsors/aandergr>`__，了解如何赞助 Instaloader 的开发！

.. current-sponsors-end

我们很高兴能将 Instaloader 分享给全世界，并为吸引了如此活跃且充满动力的社区感到骄傲，许多用户与我们分享他们的建议和想法。时不时地请社区赞助一杯啤酒或咖啡，很可能会进一步激发我们对 Instaloader 开发的热情。

| 对于捐款，我们提供了 GitHub 赞助页面、PayPal.Me 链接和比特币地址。
|  GitHub 赞助：`在 GitHub 赞助 @aandergr <https://github.com/sponsors/aandergr>`__
|  PayPal：`PayPal.me/aandergr <https://www.paypal.me/aandergr>`__
|  BTC：1Nst4LoadeYzrKjJ1DX9CpbLXBYE9RKLwY

免责声明
----------

.. disclaimer-start

Instaloader 与 Instagram 或其任何关联公司或子公司没有任何关联、授权、维护或背书。这是一个独立的非官方项目。使用风险自负。

Instaloader 根据 MIT 许可证授权。有关更多信息，请参阅 ``LICENSE`` 文件。

.. disclaimer-end
