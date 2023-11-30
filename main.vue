<div class="menu"><p class="username">username</p><p class="emailUser">emailUser</p><div @click="logout" class="logout">Logout</div></div><div @click="menu" class="toglerMenu"><div class="line"></div><div class="line"></div></div>.menu {
    position: absolute;
    top: 0;
    height: 100%;
    width: 70%;
    transform: translateX(-999px);
    background-color: #363b5c;
    transition: transform 500ms ease-in-out;
    will-change: transform;
    box-shadow: 150px 0px 10px rgba(134, 134, 134, 0.3);
    z-index: 5;
}

.toglerMenu {
    z-index: 999;
    width: 80px;
    height: 80px;
    position: absolute;
    right: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.line {
    width: 50px;
    height: 3px;
    margin: 5px 0;
    display: block;
    background-color: black;
    transition: all 500ms ease-in-out;
}

.togled {
    display: none;
}

.togled:first-child {
    position: absolute;
    display: block;
    transform: rotate(45deg);
}

.togled:last-child {
    display: block;
    transform: rotate(-45deg);
}

.active {
    transform: translateX(0);
}

.menu {
    display: flex;
    flex-direction: column;
    justify-content: end;
    align-items: center;
    color: #ffffff;
}



menu() {
    const xd=document.querySelector('.menu');
    const togle=document.querySelectorAll('.line');

    xd.classList.toggle('active');

    togle.forEach(element=> {
            element.classList.toggle('togled');
    });
}
