<!-- 练习功能页面 -->
<template>
  <div>
    <div class="calculator">
      <!-- 头部 -->
      <div class="calculator_title">
        <p style="margin-left:10px;padding: 8px 0;">计算器</p>
        <div class="calculator_btn">
          <p>一</p>
          <p>口</p>
          <p>ゑ</p>
        </div>
      </div>
      <!-- 显示区域 -->
      <div class="area">
        <div class="calculate_show">111</div>
        <div class="area_show">9</div>
      </div>
      <!-- 按钮区域 -->
      <div class="btn_district">
        <table>
          <tr>
            <td>%</td>
            <td>CE</td>
            <td>C</td>
            <td>◀✘</td>
          </tr>
          <tr>
            <td>×</td>
            <td>✘</td>
            <td>✘☩</td>
            <td>%</td>
          </tr>
          <tr>
            <td>7</td>
            <td>8</td>
            <td>9</td>
            <td>x</td>
          </tr>
          <tr>
            <td>4</td>
            <td>5</td>
            <td>6</td>
            <td>—</td>
          </tr>
          <tr>
            <td>1</td>
            <td>2</td>
            <td>3</td>
            <td>+</td>
          </tr>
          <tr>
            <td>+/-</td>
            <td>0</td>
            <td>.</td>
            <td>=</td>
          </tr>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      m: null
    };
  },
  mounted() {}
};
</script>

<style lang='less' scoped>
.calculator {
  width: 320px;
  background-color: #e6e6e6;
  margin: 0 auto;
  cursor: pointer;
  // 头部
  .calculator_title {
    display: flex;

    justify-content: space-between;
    .calculator_btn {
      display: flex;
      p {
        width: 50px;
        padding: 8px 0;
        &:hover {
          background-color: #cfcfcf;
          &:last-child {
            background-color: #e81123;
          }
        }
      }
    }
  }
  // 显示区域
  .area {
    height: 100px;
    text-align: right;
    padding: 0 6px;
    .calculate_show {
      align-self: flex-start;
      width: 100%;
      height: 50px;
      line-height: 80px;
    }
    .area_show {
      width: 100%;
      height: 50px;
      font-size: 40px;
    }
  }
  // 按钮区域
  .btn_district {
    background-color: #fff;
    table {
      tr {
        td {
          width: 80px;
          height: 50px;
          border: 3px solid #e4e4e2;
          &:hover {
            background-color: #d5d5d3;
          }
        }
      }
    }
  }
}
</style>
