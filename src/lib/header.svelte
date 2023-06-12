<script>
    import login from "$lib/assets/login.png";
    import logo from "$lib/assets/logo.jpg";
</script>

<header>
    <div class="logo"><img src={logo} alt=""></div>
    <h1>Chesscraft's Blog</h1>
    <div class="login"><img src={login} alt=""></div>
</header>
<!-- <a href="https://www.flaticon.com/free-icons/login" title="login icons">Login icons created by Freepik - Flaticon</a> -->


<style>
    header{
        width: 100%;
        background: rgb(30,30,30);
        height: 100px;
        -webkit-box-shadow: inset 0 0 40px 0px dimgrey;
        box-shadow: inset 0 0 40px 20px black;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 30px;
        box-sizing: border-box;
        border: 5px solid black;
    }

    .logo{

        transform: scale(1.25);
    }

    img{
        max-height: 50px;
        max-width: 50px;
        border-radius: 100px;
        border: 5px solid black;
    }

</style>