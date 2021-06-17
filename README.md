# StudyRecord： 如何将从后端接口获得的数据插入到table表格中

## 1.定义数据对象
    $(document).ready(function () {
      // 定义数据对象列表（假设下面就是后端接口给的数据）
      var table_data = [
        {
          name: "大兴机场",
          address: "浦城-梅州、兴国-泉州",
          car_type: "捷豹",
          user: "张三",
          date_start: "2012-12-9",
          use_time: "10",
          state: "待审核"
        },
        {
          name: "1大兴机场",
          address: "浦城-梅州、兴国-泉州",
          car_type: "捷豹",
          user: "张三",
          date_start: "2012-12-9",
          use_time: "10",
          state: "待审核"
        },
        {
          name: "2大兴机场",
          address: "浦城-梅州、兴国-泉州",
          car_type: "捷豹",
          user: "张三",
          date_start: "2012-12-9",
          use_time: "10",
          state: "待审核"
        },
        {
          name: "大兴机场",
          address: "浦城-梅州、兴国-泉州",
          car_type: "捷豹",
          user: "张三",
          date_start: "2012-12-9",
          use_time: "10",
          state: "待审核"
        },
        {
          name: "1大兴机场",
          address: "浦城-梅州、兴国-泉州",
          car_type: "捷豹",
          user: "张三",
          date_start: "2012-12-9",
          use_time: "10",
          state: "待审核"
        },
        {
          name: "2大兴机场",
          address: "浦城-梅州、兴国-泉州",
          car_type: "捷豹",
          user: "张三",
          date_start: "2012-12-9",
          use_time: "10",
          state: "待审核"
        },{
          name: "大兴机场",
          address: "浦城-梅州、兴国-泉州",
          car_type: "捷豹",
          user: "张三",
          date_start: "2012-12-9",
          use_time: "10",
          state: "待审核"
        },
        {
          name: "1大兴机场",
          address: "浦城-梅州、兴国-泉州",
          car_type: "捷豹",
          user: "张三",
          date_start: "2012-12-9",
          use_time: "10",
          state: "待审核"
        },
        {
          name: "2大兴机场",
          address: "浦城-梅州、兴国-泉州",
          car_type: "捷豹",
          user: "张三",
          date_start: "2012-12-9",
          use_time: "10",
          state: "待审核"
        }

      ];
 ## 2.创建表格的tbody并将数据写入
      // 创建表格的tbody结点
      var tbody = document.createElement("tbody");
      // 遍历数据列表
      for (var emp of table_data) {
        // 对每条数据新建表格行
        var tr = tbody.insertRow();
        // 遍历每条数据的所有数据项
        for (var pname in emp) {
          // 给每个数据项新建表格单元
          var cell = tr.insertCell(-1);
          // 将数据写入表格单元
          cell.innerHTML = emp[pname];
        }
      }
      
  ## 3.将创建好的tbody插入到对应表格并渲染
      // 将创建好的tbody插入到对应表格
      var table_ele = document.getElementById("tab-table-1");
      table_ele.appendChild(tbody);
      // 用表格插件函数渲染
      $('#tab-table-1').DataTable();
      $('#tab-table-2').DataTable();

    });

 
