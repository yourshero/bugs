# bugs
### 1.html()获取dom内容,进行等值判断时,需要进行去空格.否则if里面 '==' 判断不生效
    $('.dis-title').each(function(){
			let dis_title = $(this).html().trim();//trim() 删除字符串开始和末尾的空格
			//专题研究班
			if(dis_title=="专题研究班"){
				$(this).html(dis_title+'<span>(小班毕业后选修加入)</span>');
			}
		})

