<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Controle Financeiro Familiar - Mobile</title>

<style>
body{
font-family:Arial, sans-serif;
background:#eef2f7;
margin:10px;
}

h1{
text-align:center;
margin-bottom:5px;
}

.card{
background:white;
padding:12px;
margin-bottom:15px;
border-radius:10px;
box-shadow:0 2px 6px rgba(0,0,0,0.08);
}

.header-bar{
display:flex;
justify-content:space-between;
align-items:center;
}

button{
padding:8px;
margin-top:8px;
border:none;
border-radius:6px;
background:#2d6cdf;
color:white;
}

button.small{
padding:4px 6px;
font-size:12px;
background:#6c757d;
}

button.delete{
background:#dc3545;
padding:4px 6px;
font-size:12px;
}

table{
width:100%;
border-collapse:collapse;
font-size:14px;
}

th,td{
border:1px solid #ddd;
padding:6px;
}

th{
background:#f1f3f5;
}

input,select{
width:100%;
padding:5px;
border:1px solid #ccc;
border-radius:5px;
}

.summary{
display:grid;
grid-template-columns:1fr 1fr;
gap:10px;
}

.box{
padding:10px;
border-radius:10px;
color:white;
white-space:pre-line;
}

.income{background:#198754;}
.expense{background:#dc3545;}
.balance{background:#0d6efd;}

.alert{
font-weight:bold;
margin-top:10px;
}

.hide{
display:none;
}

</style>
</head>

<body>

<h1>Controle Financeiro Familiar</h1>

<div class="card">
<div class="header-bar">
<h2>Renda Mensal</h2>
<button class="small" onclick="toggle('incomeBox')">Ocultar/Exibir</button>
</div>

<div id="incomeBox">
<table>
<tr><th>Pessoa</th><th>Salário</th></tr>
<tr><td>Edson</td><td><input id="salEdson" type="number" value="3922.48"></td></tr>
<tr><td>Priscila</td><td><input id="salPriscila" type="number" value="2141.64"></td></tr>
</table>
</div>
</div>

<div class="card">
<div class="header-bar">
<h2>Registrar Despesa</h2>
<button class="small" onclick="toggle('expenseBox')">Ocultar/Exibir</button>
</div>

<div id="expenseBox">
<table id="expenseTable">
<tr>
<th>Data</th>
<th>Pessoa</th>
<th>Categoria</th>
<th>Descrição</th>
<th>Valor</th>
<th>Ação</th>
</tr>
</table>
<button onclick="addExpense()">+ Despesa</button>
</div>
</div>

<div class="card">
<div class="header-bar">
<h2>Ganhos Extras</h2>
<button class="small" onclick="toggle('incomeExtraBox')">Ocultar/Exibir</button>
</div>

<div id="incomeExtraBox">
<table id="incomeTable">
<tr>
<th>Data</th>
<th>Pessoa</th>
<th>Descrição</th>
<th>Valor</th>
<th>Ação</th>
</tr>
</table>
<button onclick="addIncome()">+ Ganho</button>
</div>
</div>

<div class="card">
<div class="header-bar">
<h2>Filtro</h2>
<button class="small" onclick="toggle('filterBox')">Ocultar/Exibir</button>
</div>
<div id="filterBox">
<input type="month" id="monthFilter">
</div>
</div>

<div class="card">
<div class="header-bar">
<h2>Resumo Financeiro</h2>
<button class="small" onclick="toggle('summaryBox')">Ocultar/Exibir</button>
</div>

<div id="summaryBox">
<div class="summary">
<div class="box income" id="incomeTotal"></div>
<div class="box expense" id="expenseTotal"></div>
<div class="box balance" id="balance"></div>
</div>

<p>Despesas Edson: <span id="edsonTotal"></span></p>
<p>Despesas Priscila: <span id="priscilaTotal"></span></p>

<p class="alert" id="alert"></p>
</div>
</div>

<script>

function toggle(id){
document.getElementById(id).classList.toggle('hide')
}

function addExpense(data={}){
let table=document.getElementById("expenseTable")
let row=table.insertRow()
row.innerHTML=`
<td><input type='date' value='${data.date||""}'></td>
<td>
<select>
<option>Edson</option>
<option>Priscila</option>
</select>
</td>
<td><input value='${data.cat||""}'></td>
<td><input value='${data.desc||""}'></td>
<td><input type='number' value='${data.val||""}'></td>
<td><button class='delete' onclick='if(confirm("Excluir?")){ this.parentElement.parentElement.remove(); update(); save(); }'>X</button></td>
`
if(data.person) row.querySelector("select").value=data.person
}

function addIncome(data={}){
let table=document.getElementById("incomeTable")
let row=table.insertRow()
row.innerHTML=`
<td><input type='date' value='${data.date||""}'></td>
<td>
<select><option>Edson</option><option>Priscila</option></select>
</td>
<td><input value='${data.desc||""}'></td>
<td><input type='number' value='${data.val||""}'></td>
<td><button class='delete' onclick='if(confirm("Excluir?")){ this.parentElement.parentElement.remove(); update(); save(); }'>X</button></td>
`
if(data.person) row.querySelector("select").value=data.person
}

function getIncome(){
let edson=Number(document.getElementById("salEdson").value)
let priscila=Number(document.getElementById("salPriscila").value)

let extra=0
let rows=document.querySelectorAll("#incomeTable tr")
rows.forEach((r,i)=>{
if(i==0)return
let val=Number(r.querySelector("input[type=number]").value)
extra+=val
})

return edson+priscila+extra
}

function update(){
let month=document.getElementById("monthFilter").value

let total=0,edson=0,priscila=0

let rows=document.querySelectorAll("#expenseTable tr")
rows.forEach((row,i)=>{
if(i==0)return
let inputs=row.querySelectorAll("input")
let person=row.querySelector("select").value
let date=inputs[0].value
let val=Number(inputs[3].value)
if(!date)return
if(month && !date.startsWith(month)) return

total+=val
if(person=="Edson") edson+=val
if(person=="Priscila") priscila+=val
})

let income=getIncome()
let balance=income-total

// ===== RESUMO FORMATADO =====
document.getElementById("incomeTotal").innerText=
"Renda Total: " + income.toFixed(2)

document.getElementById("expenseTotal").innerText=
"Despesa Total: " + total.toFixed(2)

document.getElementById("balance").innerText=
"Saldo Restante: " + balance.toFixed(2)

document.getElementById("edsonTotal").innerText=
edson.toFixed(2)

document.getElementById("priscilaTotal").innerText=
priscila.toFixed(2)

let msg=""
if(total>income*0.7) msg="⚠ Atenção: despesas acima de 70% da renda"
else if(balance>2000) msg="✔ Excelente controle financeiro"
else msg="ℹ Situação estável"

document.getElementById("alert").innerText=msg

save()
}

function save(){
let data={
salEdson:document.getElementById("salEdson").value,
salPriscila:document.getElementById("salPriscila").value,
expenses:[],
income:[]
}

document.querySelectorAll("#expenseTable tr").forEach((r,i)=>{
if(i==0)return
let i2=r.querySelectorAll("input")
data.expenses.push({
date:i2[0].value,
person:r.querySelector("select").value,
cat:i2[1].value,
desc:i2[2].value,
val:i2[3].value
})
})

document.querySelectorAll("#incomeTable tr").forEach((r,i)=>{
if(i==0)return
let i2=r.querySelectorAll("input")
data.income.push({
date:i2[0].value,
person:r.querySelector("select").value,
desc:i2[1].value,
val:i2[2].value
})
})

localStorage.setItem("financeSystem",JSON.stringify(data))
}

function load(){
let data=localStorage.getItem("financeSystem")
if(!data)return

data=JSON.parse(data)

if(data.salEdson) document.getElementById("salEdson").value=data.salEdson
if(data.salPriscila) document.getElementById("salPriscila").value=data.salPriscila

if(data.expenses) data.expenses.forEach(e=>addExpense(e))
if(data.income) data.income.forEach(i=>addIncome(i))
}

document.addEventListener("input",update)
document.getElementById("monthFilter").addEventListener("change",update)

load()
addExpense()
addIncome()
update()

</script>

</body>
</html>
