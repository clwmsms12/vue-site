<template>
    <div class="container header d-flex">
        <h1><a href="#"><img src="../assets/new_logo.svg" alt=""></a></h1>
        <div class="menuList">
            <ul class="d-flex gap-3">
                <li><a href="#"><i class="fa-solid fa-magnifying-glass"></i></a></li>
                <li><a href="#"><i class="fa-light fa-user"></i></a></li>
                <li><a href="#"><i class="fa-brands fa-facebook"></i></a></li>
                <li><a href="#"><i class="fa-brands fa-instagram"></i></a></li>
                <li><a href="#"><i class="fa-brands fa-youtube"></i></a></li>
                <li><a href="#"><i class="fa-solid fa-bars"></i></a></li>
            </ul>
            <ul class="d-flex gap-5">
                <li><a href="#">제이에어코리아</a></li>
                <li><a href="#">투명경영</a></li>
                <li><a href="#">교육사업</a></li>
                <li><a href="#">기관소식</a></li>
                <li><a href="#">후원하기</a></li>
            </ul>
        </div>
    </div>
    
  
</template>

<script>
export default {

}
</script>

<style lang="scss">
    .header{
        padding: 10px 0;
        h1{
            width: 215px;height: 67px;
            align-self: center;
        }
        .menuList{
            margin-left: auto;
            ul{
                justify-content: flex-end;
                li{
                    font-size: 19px;font-weight: bold;
                }
            }
            ul{
                margin-bottom: 0;
                padding: 3px;
            }
        }
    }
</style>