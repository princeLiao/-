### 正则杂记
* <a href="https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_Expressions">https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_Expressions</a>
<table>
    <tr>
        <td>. </td>
        <td>（小数点）匹配除换行符之外的任何<strong>单个</strong>字符。</td>
    </tr>
    <tr>
        <td>(x)</td>
        <td>匹配 'x' 并且记住匹配项。括号被称为 捕获括号。
<pre><code>
foo".replace(/(foo){1,2}/,"$1")=>foo
</code>
</pre>
</td>
    </tr>
    <tr>
        <td>(?:x)</td>
        <td>匹配 'x' 但是不记住匹配项。这种叫作非捕获括号，使得你能够定义为与正则表达式运算符一起使用的子表达式。来看示例表达式 /(?:foo){1,2}/。如果表达式是 /foo{1,2}/，{1,2}将只对 ‘foo’ 的最后一个字符 ’o‘ 生效。如果使用非捕获括号，则{1,2}会匹配整个 ‘foo’ 单词。
<pre><code>
foo".replace(/(?:foo){1,2}/,"$1")=>$1
</code>
</pre>
</td>
    </tr>
</table>
