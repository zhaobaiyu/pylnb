# Python Learning Notebooks

这个仓库存放Python学习和复习巩固过程中的笔记。

Numpy、Pandas、Matplotlib基本操作的复习根据*《利用Python进行数据分析》*整理。

## Basic

这里主要是使用Python中遇到的以前不知道或不熟悉的操作。

基本的Python操作并没有整理在这里。

## Numpy

这里存放Numpy学习笔记，从最基本的操作开始。

1. Numpy 基本操作

  * 创建ndarray
	
	`ndim` `shape` `dtype`
	
	`np.zeros` `np.zeros_like` `np.ones` `np.ones_like`
	
	`np.empty` `np.empty_like` 
	
	`np.eye` `np.identity`
	
	`np.arange`
	
  * 数据类型
	
	`astype`
  
  * 索引和切片
	
	`reshape` `np.ix_`
  
  * 转置和轴对换
	
	`transpose`方法 `T`属性
	
	`swapaxes`
  
2. Numpy 通用函数和利用数组进行数据处理

  * 一元ufunc（都是numpy的方法）
  
	`abs/absolute` `fabs` `sqrt` `square`
	
	`exp` `log` `log10` `log2` `log1p`
	
	`sign` `ceil` `floor` `rint` `modf`
	
	`isnan` `isfinite` `isinf`
	
	`cos` `cosh` `sin` `sinh` `tan` `tanh`
	
	`arccos` `arccosh` `arcsin` `arcshinh` `arctan` `arctanh`
	
	`logical_not`
  
  * 二元ufunc（都是numpy的方法）
	
	`add` `substract` `multiply` `divide` `floor_divide` `power`
	
	`maximun` `fmax` `minium` `fmin`
	
	`mod` `copysign`
	
	`greater` `greater_equal` `less` `less_equal` `equal` `not_equal`
	
	`logical_and` `logical_or` `logical_xor`
  
  * 生成网格数组 
  
    `np.mashgrid`
	
  * 将条件逻辑表述为数组元算 
  
	`np.where`
	
  * 数学和统计方法(数组的方法，不是numpy的方法)
  
    `mean` `sum` `std` `var` 
	
	`min` `max` `argmin` `argmax`
	
	`cumsum` `cumprod`
	
  * 用于布尔型数组的方法（数组的方法）
    
	`any` `all`
	
  * 排序
  
    `np.sort` `sort`
	
  * 数组的集合运算（numpy的方法）
  
    `unique(x)` `intersect1d(x,y)` `union1d(x,y)` `in1d(x,y)`
	
	`setdiff1d(x,y)` `setxor1d(x,y)`
	

## 注意事项

* 设置 notebook 输出每一行，而不是只有最后一个

	```
	from Ipython.core.interactiveshell import InteractiveShell
	Interactiveshell.ast_node_interactivity = 'all'
	```
	
* matplotlib 图表中输出中文（仅用于Ubuntu）

	matplotlib 配置文件的修改不适用于ttc字体，而Linux下的开源字体多为ttc类型，真让人纠结，所以还是直接在 notebook 里导入字体吧。以下为Ubuntu下的Noto Sans CJK（思源）字体。
	```
	from matplotlib.font_manager import FontProperties
	zhfont = FontProperties(
	    fname='/usr/share/fonts/opentype/noto/NotoSansCJK-Regular.ttc')
	# 具体使用的时候，在中文后面加上fontproperties，如：
	plt.title('模型复杂度', fontproperties=zhfont)
	```
	
