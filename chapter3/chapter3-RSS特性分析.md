# RSS 特性分析
基于Wlan位置指纹的室内定位技术是目前应用的最为广泛的室内定位技术。而RSS信号强度则是建立指纹库的一个重要的指标，定位的性能在很大的程度上是依靠建库的准确性。也就是RSS信号强度的稳定性。而RSS信号强度与室内环境等诸多的因素有关，为了提高和研究定位系统的性能，分析和研究一些影响RSS信号强度的因素是非常有必要的。RSS信号强度的时间分布，RSS信号强度随着时间而变化。另外，室内障碍物的阻挡，人员的活动，接收设备的不同朝向等都会影响接收到的RSS信号强度。
  本章会介绍实验环境，实验的大量的数据都是在该实验环境下采集的。并对采集的大量样本进行分析统计，总结出RSS的分布规律。

##实验环境
在进行 WLAN 信号的特性之前，首要的任务就是找一个合适的无线网络环境，所有的指纹数据的采集和测量、定位的实验都将在这个环境中进行。本文的实验环境是在北京工业大学软件学院八楼。整个八楼都被802.11无线局域网覆盖，八楼的平面图如下所示：

## RSS 信号强度特性
相比与室外而言，室内的环境更加复杂。室外的环境相对来说简单，只要不是有建筑物遮挡的地方一般来说就都可以完成定位。而且室外定位的精确度一般来说是不需要那么高，只需要大概能知道自己的位置在哪就可以完成需要。但是室内的定位对精度的要求就高的多，因为室内的范围相对于室外来说就小的多。在室外，10米以内的精度完全就可以满足需要，但是在室内1米的误差都可以把人的位置从一个商家定位到另一个商家。所以定位精度是室内定位性能的一个很重要的一个方面。而定位的实现基本上是以来 RSS 信号来实现的，下面就从不同的方面来分析 RSS 的各个特性：

### RSS 信号强度分布特性
RSS的信号不是一直都维持在一个固定的RSS值上，信号值有可能会随着时间的变化而有不同的波动，下面就从不同的时间段来分析RSS信号值波动的规律。


### 人员流动对 RSS 信号强度的影响
RSS信号值会收到障碍物的阻挡而产生信号波动，而人员流动则是室内最为常见的一个信号阻挡方式，下面的分析展示了人员的流动对RSS信号值的影响。

### 设备朝向对 RSS 强度的影响
在采集的过程中，设备朝向也是一个会影响RSS信号值的一个因素，因为在设备不同的朝向时，身体也会对某个方向的信号产生遮挡。这样也就会对信号产生一定的影响。

### 样本数量对 RSS 强度的影响
RSS信号会随着时间发生不同程度的波动，所以在采集的过程中，样本的数量也会是一个影响指纹库的一个因素。


## RSS 处理方式

### 确定性处理方法
微软的经典的 RADAR 系统对信号的值的处理就是采用的确定性的处理方法。是一种相对来说简单的定位技术。其基本的原理就是将一个采集点多次采集之后的数据进行均值处理，均值的方式可以有多种，例如简单的算术平均值，均值／方差法。经这些方法处理后的数据就可以存进数据库作为定位的一个离线库。

### 概率处理方法
确定性方法处理离线数据简单，计算量少，但是却减小了接收到的信号强度因噪声而产生的动态变化。就没有办法来保持 RSS 信号的多样性。而概率的方法则是不去破坏采集到的信号的多样性，会将所有的信号都纪录下来。并将各个信号出现概率都纪录下来。从而形成一个概率库指纹库。

## 本章小结
本章主要分析了基于 WLAN 位置指纹室内定位的关键因素。在基于 WLAN 位置指纹室内定位方法中， RSS 是其中一项很重要的信息。因此，研究 RSS 信号在室内的传播特性是很有必要的，有助于提升定位系统的性能。在进行本章的研究之前，在实验环境中通过不同的方式采集了大量的 RSS 信号数据，然后在这些数据的基础之上，分别研究了 RSS 信号强度分布特性、人员流动对 RSS 信号强度的影响、设备朝向对 RSS 强度的影响、样本数量对 RSS 强度的影响等方面，这些情况在实现定位系统的时候，都有可能会碰到这些情况。