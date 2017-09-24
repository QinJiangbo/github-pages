---
title: 实习中期总结思考
date: 2017-07-10 23:36:44
thumbnail: https://obrxbqjbi.qnssl.com/blog/image/business-thinking.png
tags:
	- 阿里巴巴
	- 实习总结
categories:
	- 经验感悟
	- 心灵港
keywords:
	- 阿里巴巴
	- 实习总结
---
一转眼已经实习一个多月了，收获很大，不管是从技术上还是从业务上。对于自身的视角有了一个更加全面地开拓，变得更加open了。但是从这一次的中期Review来看，还是存在一些盲点和不足的地方，这些都是需要值得注意和警惕的，也是下一步工作中必须踏实完成和改进的地方。

主要从两个方面来总结，一个是取得的收获，另一个是存在的不足。

### 取得的收获

最先接触的就是WebX开发框架，WebX是一个非常优秀的MVC开发框架，采用约定大于配置的思想，减少了各方（后台接口开发，前端模板开发，UI设计等等）的沟通成本，并行开发模式提升了整体的开发效率。这段时间关于WebX的学习分为了几个阶段，首先是看文档初步了解WebX开发框架是什么，各个组件模块有什么用；其次是自己对着开源的WebX网站编写了一个Demo，并成功运行；然后再看看在项目中我们是如何使用WebX框架的，具体用到了哪些功能模块；最后就是结合WebX的源码理解整个WebX框架的设计模式和架构。对照着Spring MVC开发框架来看的话，二者还是存在一些相同点的，比如二者都是独立的MVC开发框架，都可以依赖Spring IOC容器来实现Bean依赖的管理，都有拦截器的概念。不同点其实也有很多，首先是Spring MVC是基于对Servlet的封装，然后实现了请求的路由，而WebX是基于对Filter的封装，WebX选择Filter是因为它可以返还控制权（实际上是一个责任链模式的体现），而Servlet不能返还控制权；另外一点就是RESTful风格的URL请求路由，Spring MVC支持RESTful风格而WebX不支持，现在好像WebX加了一个拓展包用来支持RESTful风格路由了；对于拦截器二者其实差不多，只不过Spring MVC称之为interceptor而WebX称之为pipeline，都可以针对不同的请求制定不同的执行方式。学习WebX也是对自己关于MVC框架认识的一个拓展，收获很大。

后面有陆陆续续学习了集团的几个中间件，包括HSF，Pandora，Pandora Boot， Alitomcat，Tengine，Notify，Tair，Config Server，Diamond以及TDDL等，中间件的学习花了两个星期的时间。当时和各位师兄交流之后，决定按照先学会如何使用，然后在项目中将其灵活运用，最后再**深挖**的思路去学习。由于文档非常完备，因此学习的比较快，同时针对每一个中间件都做了相应的Demo来巩固自己的理解，收获很大。但是完成这些其实也只是停留在了师兄们建议的第二步，在项目中实际运用，距离深挖还是有一定的差距。

对于业务方面来讲，由最初的对伙拼项目完全陌生到现在能基本熟悉整个业务流程，还是有一些收获。对业务的学习主要体现在三个方面，一个是@博善师兄带着做几个项目小需求来理解整个项目，另一个是@博善师兄结合具体的业务场景给我介绍相应的业务逻辑和业务流程，最后一个就是自己针对伙拼项目以前的项目文档来学习和理解现有的业务。其实收获就是对于整个业务架构有了一个最基本的认识。

关于集团的各个项目管理工具以及项目发布系统，比如aone，aenv，psp等，都是随着需求的开发不断向前进展而逐渐熟悉的，现在基本上能比较熟练的使用相应的功能。由于系统依然还是非常复杂的，所以后续还是要花时间去了解一些其他能够快速提升自己的工作效率的功能。

### 存在的不足

虽然取得了一些收获，但是存在的不足还是非常明显的。下面分别从技术上和业务上来说。

技术上来说的话，还没有达到师兄们提出的深挖这个层次，其实对于任何一门技术，不能只求如何取用，更加要知道怎么实现的，知道如何实现的比知道如何使用收获大的多。对于WebX来说，目前虽然知道WebX如何使用，但是还不能够非常完整地说出WebX底层的实现机制，请求是如何进入如何被处理，最后是如何返回的，整个WebX的架构是怎么样的等等。这些都是需要继续深入学习和理解的。后面的话我会针对WebX的学习写一到两篇自己的深入学习和深入理解的文章。

对于中间件的学习也是如此，中间件可以说是集团所有业务的一个最核心的支撑了，不管是双十一还是我们伙拼的大促，无时不刻都在使用集团的中间件作支撑。因此，用好中间件是基本要求，但是对于中间件背后原理的理解也是非常重要的。现在项目中使用最多的中间件就是HSF，Tair， Notify以及TDDL。做Review的时候还提到了Dubbo和MetaQ，关于这两个中间件我会再花时间多多学习和深入理解。目前对于HSF，Tair以及Notify底层的实现还是理解不够的，对于Tair可能还有所了解，因为可以和Redis做一个简单的对比，但也还是要重点去了解，去学习。HSF和Dubbo的对比，MetaQ和Notify的对比这些都是要在自己对于整个技术栈深入理解之后才能给出标准的答案。

业务上问题是这次Review当中询问的重点，主要是运营-卖家-买家的顺序来阐述的。对于业务的理解其实是不够的，对于整个商品活动报名的流程也只是最基本的一个了解，更谈不上知道后台的数据是如何在各个链路节点当中流动的细节了。在脑海中对于伙拼的业务还是需要进一步的打通，重点在于理解而不是在于死记硬背。后面在业务上还是需要多和@费斯和@博善两位师兄多多沟通，要争取全部弄懂。现在对于MKC和DA以及交易这边和我们具体在业务上存在哪些联系，具体是如何和我们进行交互的还不是很熟悉，然后对于后台小二运营工具的熟悉也不够，一方面是有些工具没有权限访问，另一方面是自己还没有接触到这一块业务。比较重要的一个地方就是数据库的设计不熟，每张表对应的是什么样的业务场景不熟悉，表中具体有哪些字段不熟悉，这一些也是后面要重点接触和理解的。

另外自身对于伙拼业务的思考不够深入，没法提出比较有建设性的意见或者建议，原因主要有两点，第一是自己首先对业务不熟悉，不知道各个部分如何组合最优化，如何改进能使业务更灵活，更完善；第二是自己对于业务这个层面的理解是缺乏的，对于业务的发展以及业务的安排没有很好的认识和思考，没法透传各种数据背后带来的价值，也就是说后面必须对数据要敏感起来。

### 几点思考

1. 技术上**深挖**的这个**深挖**到底是一个什么样的深度需要好好判断，既不能研究的太浅，也不能陷在其中不能自拔以至于耽误了正常的工作。
2. 业务的思考应该从哪些方面给出着手思考？是思考如何提升GMV还是核买数量？从技术的角度思考如何提升这些指标？从业务的角度又应该如何思考提升这些指标？