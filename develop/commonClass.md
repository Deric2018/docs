### 常用类 class

```code
flex：栅格化布局
margin-left-xs：左边距小    margin-left-sm：左边距中     margin-left-lg：左边距大
padding-left-xs：左填充小   padding-left-sm：左填充中    padding-left-lg：左填充大
margin-right-xs：左边距小   margin-right-sm：左边距中    margin-right-lg：左边距大
padding-left-xs：左填充小   padding-right-sm：左填充中   padding-right-lg：左填充大

margin-lr-xs:左右边距小     margin-lr-sm:左右边距中      margin-lr-lg:左右边距大
margin-tb-xs:上下边距小     margin-tb-sm:上下边距中      margin-tb-lg:上下边距大

padding-lr-xs:左右填充小    padding-lr-sm:左右填充中      padding-lr-lg:左右填充大
padding-tb-xs:上下填充小    padding-tb-sm:上下填充中      padding-tb-lg:上下填充大


```

### 表格高度封装

```code
computed: {
      tableHeight() {
        // 括号参数为正整数 n，返回高度 = 屏幕可视高度 - n * 50
        return this.$baseTableHeight(0);
      },
 },
PS：括号里的数字越大，表格高度越低

```

```code
// 表格高度自适应指令自定义
Vue.directive("tableHeight", {
  inserted(el, _binding, vnode) {
    const paginationRef = vnode.context.$refs.paginationRef;
    const calculateHeight = () => {
      // 获取调用传递过来的数据
      const { value } = _binding;
      // 获取距底部距离（用于展示页码等信息）
      const customHeight = (value && value.customHeight) || 20;
      const paginationHeight = paginationRef ? 50 : 0;

      // 计算列表高度
      const height =
        window.innerHeight -
        el.getBoundingClientRect().top -
        customHeight -
        paginationHeight;
      // 设置高度
      el.style.height = height + "px";
    };
    // calculateHeight();
    const debouncedCalculateHeight = _.debounce(calculateHeight, 100);
    debouncedCalculateHeight();
    window.addEventListener("resize", debouncedCalculateHeight);
    el.__vueHeightDirective__ = debouncedCalculateHeight;
  },
  unbind(el) {
    window.removeEventListener("resize", el.__vueHeightDirective__);
    delete el.__vueHeightDirective__;
  },
});


// 表格高度自适应指令用法
<div v-tableHeight>
    <el-table
      class="tableClass"
      height="100%"
      ...
    >
    ...
</div>

```

### lodashjs 常用工具类

```
<span>去除数组array中的最后一个元素</span>
this.$baseLodash.initial([1, 2, 3])
//输出 => [1, 2]

<span>返回数组 array的第一个元素</span>
this.$baseLodash.head([1, 2, 3])
//输出 => 1

<span>合并数组</span>
this.$baseLodash.concat([1],[2])
//输出  => [1,2]

<span>左切片</span>
this.$baseLodash.drop([1, 2, 3],2切除的数量)
//输出  => [3]

<span>右切片</span>
this.$baseLodash.dropRight([1, 2, 3],2切除的数量)
//输出  => [1]

<span>修改拼接</span>
this.$baseLodash.join(['a', 'b', 'c'], '~');
//输出  => 'a~b~c'

<span>获取数组最后一个元素</span>
this.$baseLodash.last(['a', 'b', 'c']);
//输出  => 'c'

<span>数组去重</span>
this.$baseLodash.uniq(['a', 'b', 'a']);
//输出  => ['a','b']

<span>获取数组的最大值</span>
this.$baseLodash.max([4, 2, 8, 6])
//输出  => 8

<span>获取数组的最小值</span>
this.$baseLodash.min([4, 2, 8, 6])
//输出  => 2

<span>四舍五入(保留任意位小数)</span>
this.$baseLodash.round(4.006,2保持几位小数)
//输出  => 4.01

<span>数组内数据相加</span>
this.$baseLodash.sum([4, 2, 8, 6])
//输出  => 20

<span>返回随机数</span>
this.$baseLodash.random(0, 5)
//输出  => 0到5任意数

<span>返回数组内的随机数</span>
this.$baseLodash.sample([1, 2, 3, 4])
//输出  => 数组1到4任意数

<span>事件节流(throttle)、防抖(debounce)</span>
this.$baseLodash.debounce(func,延迟的毫秒数,options)
    func (Function): 要防抖动的函数。
      [wait=0] (number): 需要延迟的毫秒数。
      [options=] (Object): 选项对象。
      {
        leading: false, // 指定在延迟开始前调用
        trailing: true, // 指定在延迟结束后调用。
        maxWait: 1000, // 设置 func 允许被延迟的最大值
      }

```
