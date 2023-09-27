<template>
    <form>
        <label>email:</label>
        <input type="email" required v-model="email">
        <label>Password:</label>
        <input type="password" required v-model="password">
        <label>Role:</label>
        <select v-model="role">
            <option value = "front-end" >Front-End</option>
            <option value = "back-end" >Back-End</option>
            <option value = "full-stack" >Full-Stack</option>
        </select>

    
    <div class="terms">
        <input type="checkbox" required v-model="checked">
        <label>Accept terms and conditions</label>
    </div>
</form>
<p>your email was: {{ email }}</p>
    <p>your password was: {{ password }}</p>
    <p>your password was: {{ role }}</p>
    <p>Terms and conditions: {{ checked }}</p>

  
</template>

<script>
export default {
    data(){
        return{
            email: "",
            password:"",
            role:"front-end",
            checked:false
        }
    }

}
</script>

<style>
form{
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
}
label{
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
}
input, select{
    display: block;
    padding: 10px 6px;
    width:100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color:#555;
}
input[type="checkbox"]{
    display: inline-block;
    width: 16px;
    margin: 0 10px 0 0;
    position:relative;
    top:2px;
}

</style>