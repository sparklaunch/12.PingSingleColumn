<div id="shares">
    <ion-icon name="logo-facebook" />
    <ion-icon name="logo-twitter" />
    <ion-icon name="logo-instagram" />
</div>

<style>
    #shares {
        margin-bottom: 15px;
    }
    #shares > ion-icon {
        color: rgb(67, 112, 242);
        padding: 8px;
        border: 1px solid rgb(241, 243, 247);
        border-radius: 50%;
        cursor: pointer;
    }
    #shares > ion-icon:not(:last-child) {
        margin-right: 5px;
    }
    @media all and (max-width: 1440px) {
        #shares {
            text-align: center;
        }
        #shares > ion-icon {
            padding: 12px;
            font-size: 24px;
        }
        #shares > ion-icon:not(:last-child) {
            margin-right: 10px;
        }
    }
</style>
