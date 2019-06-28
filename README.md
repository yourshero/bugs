# bugs
### 1.html()获取dom内容,进行等值判断时,需要进行去空格.否则if里面 '==' 判断不生效
    $('.dis-title').each(function(){
			let dis_title = $(this).html().trim();//trim() 删除字符串开始和末尾的空格
			//专题研究班
			if(dis_title=="专题研究班"){
				$(this).html(dis_title+'<span>(小班毕业后选修加入)</span>');
			}
		})
### 2.vue2.0中用v-for遍历出的li中的@click事件在移动端无效,pc端有效
      使用了better-scroll的原因，默认它会阻止touch事件。所以在配置中需要加上click: true
     <div class="button-wrapper" v-for='item of hotCities' :key='item.id' @click='handleCityClick'>
	    <div class="button">
	      {{item.name}}
	    </div>
     </div>
     methods:{
      handleCityClick(){
        console.log(123);
      }
    },
     mounted() {
      this.scroll = new Bscroll(this.$refs.wrapper,{
        click: true
      });
    },
