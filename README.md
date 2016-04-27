# -5-3-
#代码注释中的5要与3不要
代码注释，可以说是比代码本身更重要。这里有一些方法可以确保你写在代码中的注释是友好的：  
##不要重复阅读者已经知道的内容 
能明确说明代码是做什么的注释对我们是没有帮助的。  

    // If the color is red, turn it green  
    if (color.is_red()) {  
    color.turn_green();  
    } 
##要注释说明推理和历史 
如果`代码`中的业务逻辑以后可能需要更新或更改，那就应该留下注释:)  

	  /* The API currently returns an array of items  
	  even though that will change in an upcoming ticket.  
	  Therefore, be sure to change the loop style here so that  
	  we properly iterate over an object */  
		 var api_result = {items: ["one", "two"]},  
	  items = api_result.items,  
		 num_items = items.length;  
	  for(var x = 0; x < num_items; x++) { 
	  ...  
  	} 
  	
##同一行的注释不要写得很长 
没什么比拖动水平滚动条来阅读注释更令开发人员发指的了。事实上，大多数开发人员都会选择忽略这类注释，因为读起来真的很不方便。  

		function Person(name) {  
		this.name = name;  
		this.first_name = name.split(" ")[0]; // This is just a shot in the dark here. If we can extract the first name, let's do it  
		} 
		
##要把长注释放在逻辑上面，短注释放在后面 
注释如果不超过120个字符那可以放在代码旁边。否则，就应该直接把注释放到语句上面。  

		if (person.age < 21) {  person.can_drink = false; // 21 drinking age  
		/* Fees are given to those under 25, but only in  some states. */  
		person.has_car_rental_fee = function(state) { 
		if (state === "MI") {  
		return true;  
		}  
		};  
		} 
##不要为了注释而添加不必要的注释 
画蛇添足的注释会造成混乱。也许在学校里老师教你要给所有语句添加注释，这会帮助开发人员更好地理解。但这是错的。谁要这么说，那你就立马上给他个两大耳刮子。代码应该保持干净简洁，这是毋庸置疑的。如果你的代码需要逐行解释说明，那么你最需要做的是重构。 

		if (person.age >= 21) {  
		person.can_drink = true; // A person can drink at 21  
		person.can_smoke = true; // A person can smoke at 18  
		person.can_wed = true; // A person can get married at 18  
		person.can_see_all_movies = true; // A person can see all movies at 17 
		//I hate babies and children and all things pure because I comment too much  
		} 
##注释要拼写正确 
不要为代码注释中的拼写错误找借口。IDE可以为你检查拼写。如果没有这个功能，那就去下载插件，自己动手！  
##要多多练习 
熟能生巧。试着写一些有用的注释，可以问问其他开发人员你的注释是否有用。随着时间的推移，你会慢慢懂得怎样才算是友好的注释。  
##要审查别人的注释 
在代码审查时，我们往往会忽略查看注释。不要怕要求更多的注释，你应该提出质疑。如果每个人都养成写好注释的好习惯，那么世界将会更美好。  
##总结 
注释是开发进程中非常重要的一部分，但我们不应该为了注释而注释。注释应该是有用的，简洁的，应该是对代码的一种补充。注释不应该用于逐行地解释代码，相反，它应该用于解释业务逻辑，推理以及对将来的启示。
