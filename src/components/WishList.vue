<script>
export default {}
</script>

<template>
    <div class="container-wish">
        <div class="left-section">
            <div class="title-section">
                <div class="dots">      
                    <svg xmlns="http://www.w3.org/2000/svg" height="48px" viewBox="0 -960 960 960" width="48px" fill="#5f6368"><path d="M219.55-388Q181-388 154-414.78t-27-65.09q0-39.13 27.13-65.63 27.14-26.5 65.24-26.5 38.93 0 66.28 26.73T313-480.13q0 39.13-27.45 65.63-27.45 26.5-66 26.5Zm260.58 0q-39.13 0-65.63-26.78-26.5-26.78-26.5-65.09 0-39.13 26.78-65.63 26.78-26.5 65.09-26.5 39.13 0 65.63 26.73 26.5 26.73 26.5 65.14 0 39.13-26.73 65.63-26.73 26.5-65.14 26.5Zm260.78 0q-39.04 0-66.48-26.78Q647-441.56 647-479.87q0-39.13 27.66-65.63 27.66-26.5 66.5-26.5t65.34 26.73q26.5 26.73 26.5 65.14 0 39.13-26.73 65.63-26.73 26.5-65.36 26.5Z"/></svg>
                </div>
                <h1>both of our</h1>
                <h1>wishes</h1>
            </div>
            <div class="wish-list-section">
                <h1>kita berdua punya keinginan masing-masing, kami belum bisa menepatinya tetapi dengan perjuangan kita akan wujudkan keinginan kita.
                Yang pertama adalah pergi ke swiss karena itu adalah tempat favorit kami berdua dan insya allah kami bisa pergi kesana. 
                </h1>
            </div>
        </div>
        <div class="img-section">
            <img src="../assets/WhatsApp Image 2024-12-07 at 10.34.17.jpeg" alt="img">
        </div>
    </div>
</template>

<style>
    .container-wish{
        background-color: grey;
        padding-left: 25px;
        width: 100%;
        position: relative;
    }
    .left-section{
        background-color: white;
        width: 70%;
        height: 100%;
        padding: 40px;
    }
    h1{
        font-family: sans-serif;
    }
    .title-section h1{
        font-weight: bold;
        letter-spacing: 1px;
        font-size: 55px;
    }
    .wish-list-section h1{
        padding-top: 10%;
        position: relative;
        padding-right: 10%;
        font-size: 30px;
    }
    .img-section{
        background-color: black;
        position: absolute;
        top: 50px;
        right: 50px;
        bottom: 50px;
        width: 450px;
    }
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        position: relative;
        display: flex;
        justify-content: end;
    }
    @media (max-width: 1024px) {
      .left-section {
        width: 100%;
        margin-bottom: 20px;
      }
    
      .img-section {
        width: 100%;
        height: 300px;
      }
    }
    
    @media (max-width: 768px) {
      .container-wish {
        padding: 20px;
      }
    
      .title-section h1 {
        font-size: 2rem;
        position: relative;
        z-index: 1;
        font-weight: bold;
        background: -webkit-linear-gradient(rgb(4, 0, 255), rgb(209, 209, 209));
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
      }
    
      .wish-list-section h1 {
        font-size: 1rem;
        padding-right: 5%;
        z-index: 1;
        background: -webkit-linear-gradient(#e9fe0a, #0937a2);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
      }
    
      .img-section {
        height: 250px;
        width: 150px;
        border-radius: 5px;
      }
    }
    
    @media (max-width: 576px) {
      .title-section h1 {
        font-size: 1.8rem;
      }
    
      .wish-list-section h1 {
        font-size: 0.9rem;
        padding-right: 5%;
      }
    
      .img-section {
        height: 200px;
      }
    }
</style>