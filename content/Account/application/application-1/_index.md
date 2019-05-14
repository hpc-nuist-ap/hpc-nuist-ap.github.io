---
title: "Application form"
---


<form>

  <div class="form-group">
    <label for="name">Chinese Name (中文名*)</label>
      <input type="text" name="Name" class="form-control" placeholder="Your Chinese name" required>
  </div>

  <div class="form-group">
    <label for="username">Username (用户名*)</label>
      <input type="text" name="Username" class="form-control" placeholder="Created HPC username (short, similar to Chinese Name)" required>
  </div>

  <div class="form-group">
    <label for="ID">Student/Teacher ID (学号*)</label>
      <input type="text" name="ID" class="form-control" placeholder="Your ID" required>
  </div>

  <div class="form-group">
    <label for="Phone">Phone (手机号*)</label>
      <input type="text" name="Phone" class="form-control" placeholder="Your phone number" required>
  </div>

  <div class="form-group">
      <label for="_replyto">Email address (邮箱*)</label>
      <input type="email" name="Email" class="form-control" placeholder="Your email" required>
  </div>

  <div class="form-group">
    <label for="Group">Group (类别*)</label>
    <select name="Group" class="form-control" onchange="grpSelectCheck(this);">
    <option value="">Choose...</option>
    <option id="stu" value="0">Undergraduate(本科生)</option>
    <option id="stu" value="0">Graduate(研究生)</option>
    <option id="stu" value="0">Ph.D.(博士生)</option>
    <option id="tch">Teacher(老 师)</option>
    </select>
  </div>

  <div id="sup" style="display:none;" class="form-group" required>
      <label for="Supervisor">Supervisor Category (导师*)</label>
      <select name="Supervisor" class="form-control">
        <option value="">Choose...</option>
        <!-- Sorted by initials-->
        <option>安俊琳</option>
        <option>鲍艳松</option>
        <option>卜令兵</option>
        <option>曹念文</option>
        <option>曹  乐</option>
        <option>陈爱军</option>
        <option>陈  魁</option>
        <option>陈景华</option>
        <option>陈  倩</option>
        <option>陈钟荣</option>
        <option>楚志刚</option>
        <option>刁一伟</option>
        <option>樊曙先</option>
        <option>胡方超</option>
        <option>高志球</option>
        <option>郜海阳</option>
        <option>官  莉</option>
        <option>郭凤霞</option>
        <option>韩永翔</option>
        <option>侯雪伟</option>
        <option>黄  梦</option>
        <option>黄兴友</option>
        <option>黄  乾</option>
        <option>姜海梅</option>
        <option>蒋  惠</option>
        <option>金莲姬</option>
        <option>景晓琴</option>
        <option>康汉青</option>
        <option>康  娜</option>
        <option>孔祥贞</option>
        <option>寇蕾蕾</option>
        <option>李  南</option>
        <option>李  霞</option>
        <option>李祥超</option>
        <option>李煜斌</option>
        <option>李艳伟</option>
        <option>刘  超</option>
        <option>刘玉宝</option>
        <option>刘晓莉</option>
        <option>刘银萍</option>
        <option>陆春松</option>
        <option>马晓燕</option>
        <option>毛  毛</option>
        <option>牛生杰</option>
        <option>庞小兵</option>
        <option>钱  博</option>
        <option>邱玉珺</option>
        <option>沈菲菲</option>
        <option>石广玉</option>
        <option>师  正</option>
        <option>施广全</option>
        <option>谭涌波</option>
        <option>王成刚</option>
        <option>王昊亮</option>
        <option>王红磊</option>
        <option>王  泓</option>
        <option>王剑庚</option>
        <option>王金虎</option>
        <option>王彦辉</option>
        <option>王咏薇</option>
        <option>王  震</option>
        <option>王振会</option>
        <option>魏  鸣</option>
        <option>吴  莹</option>
        <option>夏俊荣</option>
        <option>徐国杰</option>
        <option>许  丹</option>
        <option>许潇锋</option>
        <option>杨  璟</option>
        <option>杨  军</option>
        <option>杨素英</option>
        <option>杨元建</option>
        <option>杨仲江</option>
        <option>银  燕</option>
        <option>于华英</option>
        <option>于兴娜</option>
        <option>张其林</option>
        <option>张小林</option>
        <option>张元杰</option>
        <option>张云峰</option>
        <option>张泽锋</option>
        <option>赵天良</option>
        <option>赵  阳</option>
        <option>郑有飞</option>
        <option>朱  彬</option>
        <option>朱  君</option>
      </select>
  </div>

  <script>
  function grpSelectCheck(nameSelect)
  {
      if(nameSelect){
          admOptionValue = document.getElementById("stu").value;
          if(admOptionValue == nameSelect.value){
              document.getElementById("sup").style.display = "block";
          }
          else{
              document.getElementById("sup").style.display = "none";
          }
      }
      else{
          document.getElementById("sup").style.display = "none";
      }
  }
  function calDateMax()
  {
    document.getElementById('datePickerId').max = new Date(new Date().getTime() - new Date().getTimezoneOffset() * 60000).toISOString().split("T")[0];;
  }
  </script>

</form>

{{% notice warning %}}
**Expiration**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;Undergraduate: 4 years<br/>
&nbsp;&nbsp;&nbsp;&nbsp;Graduate: 4 years<br/>
&nbsp;&nbsp;&nbsp;&nbsp;Ph.D.: 6 years<br/>
&nbsp;&nbsp;&nbsp;&nbsp;Teacher: no limit<br/>
{{% /notice %}}