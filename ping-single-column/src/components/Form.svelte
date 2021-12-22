<div id="form">
    <form>
        <input type="email" name="email" placeholder="Your email address..." />
        <input type="submit" value="Notify Me" />
    </form>
</div>

<style>
    input::placeholder {
        color: rgb(200, 206, 217);
    }
    #form {
        margin-bottom: 100px;
    }
    input[type="email"] {
        border: 1px solid rgb(222, 227, 249);
        padding: 15px 25px;
        border-radius: 30px;
        margin-right: 10px;
        width: 400px;
    }
    input[type="submit"] {
        border: none;
        padding: 15px 50px;
        color: white;
        background-color: rgb(67, 112, 242);
        border-radius: 30px;
        font-weight: 600;
        box-shadow: 5px 5px 5px rgba(67, 112, 242, 0.25);
        cursor: pointer;
    }
</style>
