   # 表格隔行换色
    <script>
        //1.获取元素
        var trs = document.querySelector('tbody').querySelectorAll('tr');
        //2.利用循环绑定注册事件
        for(var i = 0;i < trs.length; i++){
            //3.鼠标经过事件 onmouseover
            trs[i].onmouseover = function(){
            this.className = 'bg';
            }
            //4.鼠标离开事件  onmouseout
            trs[i].onmouseover = function(){
                this.className = '';
            }
        }
    </script>
#     表单全选取消全选
           <script>
        //全选和取消全选做法：  让下面所有的复选框的checked属性（选中状态）跟随全选按钮即可
        //1.获取元素
        var j_caAll = document.getElementById('j_cbAll');
        var j_tbs = document.getElementById('j_tb').getElementsByTagName('input');//下面所选的复选框
        //注册事件
        j_caAll.onclick = function(){
            //this.checked 它可以得到当前的复选框的选中状态 如果是true就是选中，如果是false就是未选中
            for(var i = 0;i < j_tbs.length;i++){
                j_tbs[i].checked = this.checked;
            }
            
        }
        //2.下面复选框需要全部选中，上面全选才能选中做法 给下面所有复选框绑定点击事件，每次点击
        for(i= 0; i<j_tbs.length;i++){
            j_tbs[i].onclick = function(){
                //flag 控制全选按钮是否选中
                var flag= true;
                //每次点击下面的复选框都要循环检查4个小按钮是否全被选中
                for(var i=0;i<j_tbs.length;i++){
            if(!j_tbs[i].checked){
                flag = false;
             }
         }
        j_cbAll.checked = flag;
       }
    }
    </script>
    
