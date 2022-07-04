<template>
    <footer class="footer">
        <hr>
        <div class="footer__menu">
            <ul>
                <li class="footer__head">App</li>
                <li><a href="#">Contact</a></li>
                <li><a href="#">Brand</a></li>
                <li><a href="#">Blog</a></li>
                <li><a href="#">Community</a></li>
                <li><a href="#">Token</a></li>
                <li><a href="#">Online Store</a></li>
            </ul>
        </div>
        <div class="footer__menu">
            <ul>
                <li class="footer__head">Developers</li>
                <li><a href="#">Github</a></li>
                <li><a href="#">Documentation</a></li>
                <li><a href="#">Bug Bounty</a></li>
                <li><a href="#">Audits</a></li>
                <li><a href="#">Careers</a></li>
            </ul>
        </div>
        <div class="footer__menu">
            <ul>
                <li class="footer__head">Help</li>
                <li><a href="#">Customer Support</a></li>
                <li><a href="#">Troubleshooting</a></li>
                <li><a href="#">Guides</a></li>
            </ul>
        </div>
    </footer>
</template>

<script>
export default {

}
</script>

<style>
.footer {
    position: relative;
    bottom: 0;
    text-align: center;
    display: flex;
    justify-content: space-between;
}

hr {
    position: absolute;
    top: 0;
    width: 100%;
    height: 1px;
    border: 0;
    background: #fff;
}

.footer__menu {
    list-style: none;
    padding: 2rem 4rem;
    margin-top: 2rem;
}

li {
    margin-bottom: 10px;
    list-style: none;
}

.footer__head {
    color: var(--color-primary);
    font-size: 20px;
    text-transform: uppercase;
}

/* mobile screen */
@media (max-width: 768px) {
    .footer {
        flex-direction: column;
    }

    .footer__menu {
        margin-top: 0;
    }
}

/* tablet screen */
@media (min-width: 768px) and (max-width: 1024px) {
    .footer {
        flex-direction: row;
    }
}
</style>