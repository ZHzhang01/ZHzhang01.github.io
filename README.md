# Academic Pages
**Academic Pages is a GitHub Pages template for personal and professional portfolio-oriented websites.**

![Academic Pages template example](images/homepage.png "Academic Pages template example")

# Getting Started

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Click the "Use this template" button in the top right.
1. On the "New repository" page, enter your public repository name as "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and add your content.
1. Upload any files (like PDFs, .zip files, etc.) to the `files/` directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

See more info at https://academicpages.github.io/

## Running locally

When you are initially working on your website, it is very useful to be able to preview the changes locally before pushing them to GitHub. To work locally you will need to:

1. Clone the repository and made updates as detailed above.

### Using a different IDE
1. Make sure you have ruby-dev, bundler, and nodejs installed
    
    On most Linux distribution and [Windows Subsystem Linux](https://learn.microsoft.com/en-us/windows/wsl/about) the command is:
    ```bash
    sudo apt install ruby-dev ruby-bundler nodejs
    ```
    If you see error `Unable to locate package ruby-bundler`, `Unable to locate package nodejs `, run the following:
    ```bash
    sudo apt update && sudo apt upgrade -y
    ```
    then try run `sudo apt install ruby-dev ruby-bundler nodejs` again.

    On MacOS the commands are:
    ```bash
    brew install ruby
    brew install node
    gem install bundler
    ```
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.

    If you see file permission error like `Fetching bundler-2.6.3.gem ERROR:  While executing gem (Gem::FilePermissionError) You don't have write permissions for the /var/lib/gems/3.2.0 directory.` or `Bundler::PermissionError: There was an error while trying to write to /usr/local/bin.`
    Install Gems Locally (Recommended):
    ```bash
    bundle config set --local path 'vendor/bundle'
    ```
    then try run `bundle install` again. If succeeded, you should see a folder called `vendor` and `.bundle`.

1. Run `jekyll serve -l -H localhost` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.
    You may also try `bundle exec jekyll serve -l -H localhost` to ensure jekyll to use specific dependencies on your own local machine.

If you are running on Linux it may be necessary to install some additional dependencies prior to being able to run locally: `sudo apt install build-essential gcc make`

## Using Docker

Working from a different OS, or just want to avoid installing dependencies? You can use the provided `Dockerfile` to build a container that will run the site for you if you have [Docker](https://www.docker.com/) installed.

You can build and execute the container by running the following command in the repository:

```bash
chmod -R 777 .
docker compose up
```

You should now be able to access the website from `localhost:4000`.

### Using the DevContainer in VS Code

If you are using [Visual Studio Code](https://code.visualstudio.com/) you can use the [Dev Container](https://code.visualstudio.com/docs/devcontainers/containers) that comes with this Repository. Normally VS Code detects that a development coontainer configuration is available and asks you if you want to use the container. If this doesn't happen you can manually start the container by **F1->DevContainer: Reopen in Container**. This restarts your VS Code in the container and automatically hosts your academic page locally on http://localhost:4000. All changes will be updated live to that page after a few seconds.

# Maintenance

Bug reports and feature requests to the template should be [submitted via GitHub](https://github.com/academicpages/academicpages.github.io/issues/new/choose). For questions concerning how to style the template, please feel free to start a [new discussion on GitHub](https://github.com/academicpages/academicpages.github.io/discussions).

This repository was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License (see LICENSE.md). It is currently being maintained by [Robert Zupko](https://github.com/rjzupkoii) and additional maintainers would be welcomed.

## Bugfixes and enhancements

If you have bugfixes and enhancements that you would like to submit as a pull request, you will need to [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) this repository as opposed to using it as a template. This will also allow you to [synchronize your copy](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork) of template to your fork as well.

Unfortunately, one logistical issue with a template theme like Academic Pages that makes it a little tricky to get bug fixes and updates to the core theme. If you use this template and customize it, you will probably get merge conflicts if you attempt to synchronize. If you want to save your various .yml configuration files and markdown files, you can delete the repository and fork it again. Or you can manually patch.

---
<div align="center">
    
![pages-build-deployment](https://github.com/academicpages/academicpages.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)
[![GitHub contributors](https://img.shields.io/github/contributors/academicpages/academicpages.github.io.svg)](https://github.com/academicpages/academicpages.github.io/graphs/contributors)
[![GitHub release](https://img.shields.io/github/v/release/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io/releases/latest)
[![GitHub license](https://img.shields.io/github/license/academicpages/academicpages.github.io?color=blue)](https://github.com/academicpages/academicpages.github.io/blob/master/LICENSE)

[![GitHub stars](https://img.shields.io/github/stars/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io)
[![GitHub forks](https://img.shields.io/github/forks/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io/fork)
</div>























好的，我将构造几个简单直观的例子，来说明当 Condition 1 中的第一个条件（结果期望相等）成立时，平均处理效应（ATE）是如何实现可辨识的。
我会确保例子具备：

* 简单的变量结构（如线性模型、二元变量）
* 容易验证兼容性条件和分布一致性
* 显式说明为何只要满足第一个子条件，ATE 就能从观测数据唯一确定

我整理好后会马上告诉你。


# 结果期望等效下 ATE 可辨识的示例

为了说明在文章提出的 **Identifiability Condition（条件1）** 下，当第一条 **“结果期望等效”** 条件成立时平均处理效应（ATE）如何可辨识，下面构造几个简洁直观且易于验证的示例。每个示例都定义了明确的变量和分布，并构造出两组“兼容的”分布组合 \$(p, P)\$ 和 \$(q, Q)\$，使它们仅满足条件1的第一项（即两分布下结果的期望值相等），而另外两项条件不满足。我们将解释为何在这种情况下，即使缺少其他差异信息，ATE 仍然是可辨识的，并用通俗语言阐述其中的直觉。

## 示例 1：二值结果的混杂示例

**变量设定：** 考虑一个简单场景，没有显式协变量 \$X\$（或认为 \$X\$ 取固定值，不影响分析）。处理变量 \$T\in{0,1}\$，结果 \$Y\$ 是二值变量（例如成功=1或失败=0）。对于每个个体，有两个潜在结果：\$Y(0)\$ 表示未接受处理时的结果，\$Y(1)\$ 表示接受处理时的结果。我们假设 \$Y(0)\$ 和 \$Y(1)\$ 的取值由某种概率分布决定。

**分布结构：** 在此示例中，我们设定两个可能的因果世界（数据生成过程）\$D\_1\$ 和 \$D\_2\$，它们对应两组“兼容的”分布组合 \$(p, P)\$ 和 \$(q, Q)\$。这里，\$P\$ 和 \$Q\$ 表示 \$(X,Y(1))\$ 的分布（本例中无显式 \$X\$），\$p\$ 和 \$q\$ 表示处理赋值机制（即给定个体属性下被处理的概率）。具体如下：

* **世界 \$D\_1\$（对应 \$(p, P)\$）：**

  * \$Y(1)\$ 的分布 \$P\$: 假设个体接受处理时获得成功（\$Y=1\$）的概率较高。例如，\$P(Y(1)=1) = 0.7\$（成功率70%，失败率30%）。
  * \$Y(0)\$ 我们设定为始终为0（未处理时从不成功），以突出处理的作用。
  * 处理机制 \$p\$: 为引入混杂因素，假设处理并非随机，而是**依赖于潜在结果**。具体地，令 \$p(y)\$ 表示当潜在处理结果为 \$y\$ 时赋予处理的概率。在\$D\_1\$中，如果某人的潜在处理结果\$Y(1)\$本来是成功（\$y=1\$），赋予处理的概率较大；若潜在\$Y(1)=0\$，赋予处理的概率较小。举例而言：设定 \$p(Y(1)=1)=0.8\$，\$p(Y(1)=0)=0.2\$。也就是说，在\$D\_1\$中那些“本来会成功”的人更有可能接受处理（这是一种违反无混杂假设的情形，因为处理决策取决于潜在结果）。

* **世界 \$D\_2\$（对应 \$(q, Q)\$）：**

  * \$Y(1)\$ 的分布 \$Q\$: 为使期望相同，我们选择一个不同的结果分布，但让成功的平均概率仍是70%。例如，在\$D\_2\$中，可能潜在成功率同样为0.7，但成功与失败的分布细节不同（比如按某种不同模式分配成功的概率，但总体平均仍是0.7）。为了简单，可以先设定 \$Q(Y(1)=1)=0.7\$（即与\$P\$的边际成功率相等），后面通过处理机制调整使其分布与\$P\$不同）。
  * \$Y(0)\$ 同样设定始终为0（与\$D\_1\$相同），保证两世界在未处理结果上的期望一致（都为0）。
  * 处理机制 \$q\$: 在\$D\_2\$中，我们采用与\$D\_1\$相反的偏好分配处理。也就是说，如果某人的潜在\$Y(1)\$本来是成功，则**降低**其被处理概率；若潜在\$Y(1)=0\$，则**提高**其被处理概率。继续上述数值例子，设定 \$q(Y(1)=1)=0.2\$，\$q(Y(1)=0)=0.8\$，与\$p\$恰好相反。这样设计使得虽然\$D\_2\$中本来成功的人不太接受处理，但由于\$D\_2\$的\$Y(1)\$成功概率分布可能略有调整，我们仍确保总体成功率相同。

在这个构造下，两个世界在**观测数据**上的许多方面是无法区分的：协变量分布相同（这里无协变量，满足 \$P\_X = Q\_X\$），并且经过适当选择参数，可以使观察到的\$(T,Y)\$联合分布在两种情况下高度相似。例如，我们可以调节\$D\_2\$中\$Y(1)\$分布的形状以及\$q\$，使得在两种机制下，被处理组和未处理组中观测到成功的概率分布一致。通过精心匹配概率，我们可以做到对于每一种观测到的情形（如“某人接受处理且结果=成功”），在两个世界中出现的概率完全相同。也就是说，对于任意可能的观测组合\$(T=t, Y=y)\$，都有 \$\Pr\_{D\_1}(T=t,Y=y) = \Pr\_{D\_2}(T=t,Y=y)\$，使条件1的第二、三项都不成立（协变量边缘分布相同，且观测分布在各点上无可区别差异）。事实上，在这种设计下，\$D\_1\$和\$D\_2\$产生的**完整观测数据**分布是相同的，因此仅凭观察数据无法辨别究竟真实世界是哪一个，这体现了混杂和选择偏差带来的不识别问题。

然而，关键在于我们确保了**结果期望等效**这一条件：在\$D\_1\$和\$D\_2\$中，处理下的结果平均值**相等**。根据设置，\$E\_{P}\[Y(1)] = 0.7\$，\$E\_{Q}\[Y(1)] = 0.7\$，两者相等。同时，由于\$Y(0)\$在两世界中平均值都是0（所有个体未处理时都失败），因此**ATE**在两种情况下都是相同的：
$\text{ATE}_{D_1} = E[Y(1)] - E[Y(0)] = 0.7 - 0 = 0.7,$
$\text{ATE}_{D_2} = 0.7 - 0 = 0.7.$
尽管\$D\_1\$和\$D\_2\$在潜在数据生成机制上截然不同（一个偏向给予本来会成功者处理，另一个相反），它们所对应的ATE值均为0.7。

**可辨识性解释：** 因为任何与观测数据兼容的潜在世界（在本例中就是\$D\_1\$或\$D\_2\$)都赋予处理后结果相同的期望值，我们无需知道究竟是哪一个世界真实存在，就可以确定“在处理下平均结果”的值为0.7。进而，由于未处理结果平均值也清楚（为0），ATE可直接计算得到0.7。这意味着ATE在给定观测证据下是**单一确定**的，不受潜在混杂不确定性的影响——换言之，ATE已被识别出来。

**直觉逻辑：** 在通俗层面，这个例子表明：如果无论是哪种潜在混杂机制，所有人接受处理后的平均结局都是一样的，那么我们就**不需要**区分具体是哪种机制在起作用。即使我们无法通过协变量分布或其他细节辨别两个隐藏的情景，它们导致的**平均效果**是一致的，因此我们可以确信地声称这个共同的平均结果就是处理的作用。正如原文所述，如果两种兼容情景满足结果期望等效，“我们就完成了（辨识），因为我们关心的期望结果在两种分布下是相同的”。直观上，这相当于说：即使存在看不见的混杂，只要任何符合数据的可能世界都赋予处理相同的平均收益，那么这个平均收益就是可靠可估的，因而ATE可辨识。

## 示例 2：线性模型的潜在混杂示例

**变量设定：** 现在考虑一个带有连续结果的线性模型，并引入一个**潜在未观察变量**来产生混杂。设定一个协变量 \$U\$（未被观测到的混杂因素，例如个体的潜在健康指数），它同时影响处理决策 \$T\$ 和结果 \$Y\$。为简单起见，假设没有其他可观测协变量 \$X\$。结果模型采用线性形式：对于任意个体，

* 未处理时的结果：\$Y(0) = \alpha + \beta U + \varepsilon\_0\$
* 处理后的结果：\$Y(1) = \alpha + \beta U + \tau + \varepsilon\_1\$

其中 \$\tau\$ 表示处理对结果的“真實效应”（在该模型中假设为加性常数效应），\$\varepsilon\_0,\varepsilon\_1\$ 是独立噪声项，均值为0（例如服从正态分布）。这意味着如果个体接受处理，其结果比未接受处理时高出固定的\$\tau\$，除去混杂因子和噪声的影响。混杂因素 \$U\$ 可能影响结果（通过系数\$\beta\$）且影响处理概率。

**构造两套“兼容”分布 \$(p, P)\$ 和 \$(q, Q)\$：** 我们考虑两个不同的潜在世界，它们均符合上述模型形式但参数不同。

* **世界 \$D\_1\$（\$(p, P)\$）：**
  令处理效应为 \$\tau\_1\$，未被观测混杂 \$U\$ 在总体上服从某一分布，设 \$U \sim \mathcal{N}(0,1)\$（正态分布，均值0，方差1），且\$\beta\$ 为常数。在\$D\_1\$中，处理决策机制 \$p\$ 假设**严重混杂**：例如，\$T\$的赋值高度依赖于\$U\$，可能采取阈值策略：\$p(u) = \Pr(T=1|U=u) = \mathbf{1}{u > c}\$（某个阈值\$c\$），即当未观察变量\$U\$高于\$c\$时个体几乎必定接受处理（例如因为\$U\$代表风险更高需要治疗），低于\$c\$时几乎不接受。这违反了Overlap假设（处理决策接近确定性），也违反了无混杂（因为\$U\$未观测但影响\$T\$和\$Y\$）。

  在该世界中，\$Y(1) = \alpha\_1 + \beta\_1 U + \tau\_1 + \varepsilon\_1\$，\$Y(0) = \alpha\_1 + \beta\_1 U + \varepsilon\_0\$。处理效应为\$\tau\_1\$。我们可以计算处理下结果的期望：
  $E_{P}[Y(1)] = \alpha_1 + \beta_1 E[U] + \tau_1.$
  由于我们选取 \$E\[U]=0\$，可得 \$E\_P\[Y(1)] = \alpha\_1 + \tau\_1\$。

* **世界 \$D\_2\$（\$(q, Q)\$）：**
  我们令该世界的模型结构类似，但参数有所不同。设\$D\_2\$中的处理效应为\$\tau\_2\$，混杂\$U\$可能有不同的分布或不同对结果的影响。为了保证兼容且观测数据难以区分，我们让\$U\$在\$D\_2\$中也服从\$\mathcal{N}(0,1)\$（与\$D\_1\$相同的边际分布），系数\$\beta\_2\$可与\$\beta\_1\$不同，但\$U\$的分布和对\$T\$的影响方式类似。处理机制\$q\$同样可以采用基于\$U\$的阈值策略，但阈值可能不同或者处理概率的依赖形式略有不同（以确保观测到的\$T\$分布与\$D\_1\$相似，比如也满足近似50%的总体处理率，只是由\$U\$决定）。在\$D\_2\$中，\$Y(1) = \alpha\_2 + \beta\_2 U + \tau\_2 + \varepsilon\_1'\$，\$Y(0) = \alpha\_2 + \beta\_2 U + \varepsilon\_0'\$。

  关键之处在于，我们调节\$D\_2\$的参数使得**处理下结果的平均值与\$D\_1\$相同**。也即要求：
  $E_{Q}[Y(1)] = \alpha_2 + \beta_2 E[U] + \tau_2 = \alpha_2 + \tau_2 = \alpha_1 + \tau_1.$
  通过适当选择\$\alpha\_2\$和\$\tau\_2\$，可以满足此条件。例如，若\$D\_1\$中\$\alpha\_1=0\$且\$\tau\_1=5\$，则\$E\_P\[Y(1)] = 5\$；我们可以令\$D\_2\$中的处理效应\$\tau\_2\$较小（甚至为0），同时提高基础水平\$\alpha\_2\$，如取\$\tau\_2=0\$且\$\alpha\_2=5\$，则\$E\_Q\[Y(1)] = 5\$，实现两世界处理结果期望相等。

在上述构造下，两个世界在观测层面可能表现出非常相似的分布特征：混杂变量\$U\$未被观测，因此研究者看到的只是根据\$U\$决定的处理概率模式（例如都呈现某种与未观测特质相关的截断分配）和处理组/对照组的结果分布。如果参数选择得当，\$D\_1\$和\$D\_2\$可能产生几乎无法区分的观察数据。例如，我们可以设置\$D\_2\$使得处理组和未处理组的**边际**结果分布都与\$D\_1\$吻合（比如调整噪声方差和\$\beta\_2\$使两世界的结果方差也类似），同时协变量（这里\$U\$不可见，但如果有可见的代理协变量，也可令其分布相同）。在这种情况下，条件1的第二项 \$P\_X=Q\_X\$ 自然成立（无显性协变量或同分布），第三项关于观测分布细微差异的条件也不会触发，因为我们尽量令两世界产生的\$(T,Y)\$联合分布接近（在理想情况下，可认为对任何观测到的密度都满足 \$p(u)P(u,y) = q(u)Q(u,y)\$，只是\$u\$未观测）。

**结果期望等效：** 根据构造，\$D\_1\$和\$D\_2\$满足 \$E\_P\[Y(1)] = E\_Q\[Y(1)]\$。以上例子中，两者这个值都被调节为5（无论真实处理效应大小差异，只要基础水平相应调整，使得所有人接受处理时平均结果一致）。类似地，我们也可以确保 \$E\_P\[Y(0)] = E\_Q\[Y(0)]\$：在\$D\_1\$中\$E\[Y(0)] = \alpha\_1\$，在\$D\_2\$中\$E\[Y(0)] = \alpha\_2\$，我们已经让\$\alpha\_2 = \alpha\_1 + (\tau\_1 - \tau\_2)\$，从而使 \$\alpha\_2\$ 增加的量正好弥补处理效应的减少量，这会导致两世界中未处理结果的总体平均也相等（在上述数值例子中，\$D\_1\$有\$\alpha\_1=0\$故\$E\[Y(0)]=0\$，\$D\_2\$有\$\alpha\_2=5\$但\$\tau\_2=0\$，这样**对照组**平均结果\$E\[Y(0)]\$在\$D\_2\$也是5，与\$D\_1\$中的\$E\[Y(1)]\$相同；为了让两边\$Y(0)\$平均一致，可以进一步假定\$D\_1\$和\$D\_2\$中\$\beta U\$项均值为0，则\$E\_P\[Y(0)] = \alpha\_1\$，\$E\_Q\[Y(0)] = \alpha\_2\$，只要\$\alpha\_2 = \alpha\_1\$则二者也相等。在我们的例子里\$\alpha\_1=0, \alpha\_2=5\$显然不等，因此严格来说这里\$Y(0)\$期望不相等。但是我们也可以选择\$\alpha\_1=2.5, \tau\_1=2.5\$ 和\$\alpha\_2=5, \tau\_2=0\$，这样\$E\_P\[Y(1)] = 5, E\_Q\[Y(1)] = 5\$且\$E\_P\[Y(0)] = 2.5, E\_Q\[Y(0)] = 5\$，两世界ATE均为\$5-2.5=2.5\$。亦或调整\$D\_2\$使\$E\[Y(0)]\$也等于2.5。总之，可以通过参数使得**两个世界的ATE相等**。)

在恰当的参数配置下，我们可以实现**两种潜在世界的 ATE 值相同**，即 \$\tau\_{D\_1} = \tau\_{D\_2}\$，即使它们内在的因果结构不同。例如按照刚才括号内调整，使\$D\_1\$和\$D\_2\$均有 ATE \$=2.5\$。

**ATE 可辨识性：** 由于无论\$D\_1\$还是\$D\_2\$为真，处理的平均结果（以及未处理的平均结果）都是相同的，因而ATE在这两个兼容世界中取同一数值。换言之，在满足结果期望等效的前提下，我们已经排除了“潜在另一个数据生成过程会给出不同ATE值”的可能性。因此，观察到的数据无法区分\$D\_1\$或\$D\_2\$并不妨碍我们推断ATE，因为这两个候选世界对ATE的预测**完全一致**。ATE的识别在理论上是保证的：给定观测分布，只要它符合我们的模型类假设，那么所有符合该观测分布的潜在真相都赋予相同的ATE值，我们就可以将其视为真实的因果效应。

**直觉解释：** 这个线性模型示例展示了如下道理：**平均因果效应的可识别不一定需要传统的无混杂或重叠假设，只要我们确信所有可能的隐藏情况对“处理的平均结果”有相同的预测。**在\$D\_1\$和\$D\_2\$中，我们分别设置了不同的处理效应和基础结果水平，但**巧妙地保持了处理组和对照组结果的总体均值不变**。因此，即便研究者不知道实际的混杂程度（因为\$U\$不可见）或处理机制，他依然能够确定：如果让所有人都接受处理，平均结果将是某个固定值（比如5）；如果无人接受处理，平均结果将是另一个固定值（比如2.5）。这些值在不同潜在真相下没有差别，因而我们可以自信地计算ATE（例如5-2.5=2.5）。通俗地说，当潜在的因果模型尽管不同，却**不得不**给出同样的平均效果时，我们就击破了不确定性，对平均处理效应有了唯一确定的估计。

## 示例 3：潜在子人群模型的等价示例

**变量设定：** 最后我们考虑一个**潜在子人群**模型，展示即使结果分布有复杂的异质性，但只要平均值相同，ATE 仍然可辨识。假设总体由两类隐藏的亚组组成（不可直接观测到组别）。组别影响处理结果分布，但总体的平均结果由两组混合决定。令潜在组别指示符为\$Z\in{A, B}\$，未观察到\$Z\$。我们定义各组在处理下的结果分布不同。

**构造 \$(p, P)\$ 和 \$(q, Q)\$：**

* **世界 \$D\_1\$（两类人群组成）：**  在处理下，假设组\$A\$的人一定得到某一固定结果，组\$B\$的人得到另一固定结果。例如：组\$A\$个体接受处理后\$Y(1)=0\$（始终失败），组\$B\$个体接受处理后\$Y(1)=8\$（始终成功较高值）。设组\$A\$占总体的比例为\$40%\$，组\$B\$占\$60%\$。那么在\$D\_1\$中处理下结果的总体分布是两点混合：40%概率为0，60%概率为8，平均值为 \$E\_P\[Y(1)] = 0\times0.4 + 8\times0.6 = 4.8\$。未处理时，为简化，我们可以假定两组都不会成功（\$Y(0)=0\$无论\$A\$或\$B\$），这样\$E\_P\[Y(0)] = 0\$，ATE$\_{D\_1} = 4.8 - 0 = 4.8\$。处理赋值机制\$p\$可以假设为随机（每个人有一定概率接受处理），或者也可以依赖于组别\$Z\$（例如让某一组更可能接受处理），但由于\$Z\$不可见且我们稍后匹配另一个世界的分布，此处不妨设\$p\$为简单的固定概率（如50%概率接受处理），确保Overlap。

* **世界 \$D\_2\$（不同异质性的两类人群）：** 我们设定另一种隐藏组成，使得处理下结果平均仍为4.8，但组构成或结果值不同。比如，在\$D\_2\$中，令组\$A'\$占60%，组\$B'\$占40%\$^{†}\$（与\$D\_1\$的比例相反）。假设组\$A'\$接受处理后结果始终为0，与\$D\_1\$的组\$A\$相同，但现在这类人更多（60%）；组\$B'\$接受处理后结果始终为**12**（一个更高的值），但这类人仅占40%。则\$D\_2\$中处理结果平均值：\$E\_Q\[Y(1)] = 0\times0.6 + 12\times0.4 = 4.8\$，恰好与\$D\_1\$相同。未处理情况下，我们同样假定所有组都得到0（即\$Y(0)=0\$），因此\$E\_Q\[Y(0)] = 0\$，ATE$\_{D\_2} = 4.8 - 0 = 4.8\$。处理机制\$q\$可以与\$p\$类似假设为随机50%。

\$^{†}\$ *（这里用 \$A'\$ 和 \$B'\$ 指代 \$D\_2\$ 中的隐藏组，以区别于 \$D\_1\$ 的 \$A,B\$ 组；需要强调的是，外部观察者并不知道这些组的存在，它们只是我们构造世界的隐含分类。）*

在上述两个世界中，处理下结果的**整体分布形状**其实是不同的：\$D\_1\$世界中观察到接受处理者的结果要么是0要么是8，\$D\_2\$世界中接受处理者的结果要么是0要么是12。然而，由于组比例相反地调整，这两个分布的**总体均值**相同，都是4.8。同时，两世界未处理结果均为0平均。因此，从平均效果来看，两个世界的ATE同为4.8。

现在，如果我们只根据观察数据，很难直接区分这两种情况，因为我们通常无法直接观察到潜在组\$Z\$，只看到部分人的处理结果。假如处理是随机的一半人，则我们可能观察到处理组的结果有两种值（0和8或0和12）但比例不同，可能通过统计检验能发现差异。然而，如果我们进一步考虑更一般的情况：例如处理并非纯随机，而是稍微倾向于某组，使得在观察数据中0和高值出现的频率分布更趋近，这会让这两种世界产生的**观测分布更加相似**。在极端情况下，研究者可能无法确定高结果值的出现是因为较大效应作用于较少人，还是较小效应作用于较多人。条件1的第二项在此依然没有提供帮助（两个世界协变量边际分布同为整体人口，无差异），第三项也可能难以利用（因为如果频率被设计得很接近，观测密度上难以找到显著差别点）。

**结果期望等效：** 关键在于，无论是\$D\_1\$还是\$D\_2\$，**处理下结果的总体期望**都是4.8，满足条件1的第一子条件。此外，未处理结果期望同为0。在这个条件下，平均处理效应ATE在两个备选世界中完全一致，均为4.8。

**ATE 可辨识性：** 因为所有能够吻合观察数据的潜在世界都给予了相同的ATE值，我们可以断言ATE就是4.8。换言之，即使结果分布的细节（比如成功由谁贡献，是更多人稍低的成功还是更少人更高的成功）在不同世界中不同，这些差异不影响平均效果的值。在这种情形下，ATE对观察者来说是**识别出来的**：任何与数据一致的假设都会导向同样的平均因果效应估计。

**直觉说明：** 这个潜在子人群的例子体现出“**均值掩盖了异质性**”的思想：即便不同机制导致了结果的不同分布形态，只要它们的平均值一致，我们关心的平均处理效应就不会改变。对于政策评估者来说，这意味着无需了解隐藏人群的细节组成，也不用知道究竟是哪一种分布在起作用——只要所有可能的情况都指向同一个平均收益，那个收益值就是可靠的。简单来说，\*\*如果任何可能的世界都不能改变处理的平均效果，那么这个效果就是辨识无疑的。\*\*即使我们无法通过数据辨别隐藏的结构，平均效果因为“结果期望等效”而固定不变，从而被成功识别。

以上三个示例共同说明了条件1中第一条要求（**结果期望等效**）的重要作用：当对于任何两个兼容的数据生成假设，处理结果的平均值都相同，则平均处理效应不会因为识别上的不确定性而改变，我们可以在观测数据的支持下确定这个唯一的ATE值。换句话说，在这种情形下，“相关并不等于因果”的困境被巧妙地规避了——因为所有相关的可能因果世界在平均因果效应这个量上达成了一致。于是，ATE 即使在其他假设（如无混杂、重叠）不满足的情况下，仍然是**可辨识**和**可推断**的。



