<hr>
<h3>📘 Lug‘at</h3>

<input type="text" id="search" placeholder="Qidirish..." onkeyup="searchWord()">

<div id="dictionary"></div>

<script>

const words = [
 {en:"Apple", uz:"Olma"},
 {en:"Book", uz:"Kitob"},
 {en:"School", uz:"Maktab"},
 {en:"Teacher", uz:"O‘qituvchi"},
 {en:"Student", uz:"O‘quvchi"},
 {en:"Learn", uz:"O‘rganmoq"},
 {en:"Speak", uz:"Gapirmoq"}
];

function showWords(list){
 let box = document.getElementById("dictionary");
 box.innerHTML="";
 list.forEach(w=>{
   box.innerHTML += 
   "<div style='text-align:left;margin:5px 0;'>"+
   "🇬🇧 "+w.en+" = 🇺🇿 "+w.uz+
   "</div>";
 });
}

function searchWord(){
 let value = document.getElementById("search").value.toLowerCase();
 let filtered = words.filter(w=>
   w.en.toLowerCase().includes(value)
 );
 showWords(filtered);
}

showWords(words);

</script>
