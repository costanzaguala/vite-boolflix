<script>
export default {
    data() {
        return {
             
        };
     },
    methods: {

    }
}
</script>

<template> 

    <header class="fixed-top">
        <nav class="navbar">
            <div class="container-fluid navbar-expand-lg">

                <img src="../assets/img/logo-gobike.png" alt="logo">

                <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar" aria-controls="offcanvasNavbar" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                
                <div class="offcanvas offcanvas-start" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
                    <div class="offcanvas-header">
                        <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
                    </div>

                    <div class="offcanvas-body">

                        <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
                            <li class="nav-item">
                            <a class="nav-link active" aria-current="page" href="#">Home</a>
                            </li>

                            <li class="nav-item">
                                <a class="nav-link active" href="#">About us</a>
                            </li>

                            <li class="nav-item dropdown">
                            <a class="nav-link active" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                                Training
                            </a>
                                <ul class="dropdown-menu">
                                    <li><a class="dropdown-item" href="#">Riding Lesson</a></li>
                                    <li><a class="dropdown-item" href="#">Another action</a></li>
                                    <li><a class="dropdown-item" href="#">Safe Driving</a></li>
                                    <li><a class="dropdown-item" href="#">Mountain Bike</a></li>
                                    <li><a class="dropdown-item" href="#">Trail Drive</a></li>
                                    <li><a class="dropdown-item" href="#">Pedaling</a></li>
                                    <li><a class="dropdown-item" href="#">All Training</a></li>
                                </ul>
                            </li>

                            <li class="nav-item">
                                <a class="nav-link active" href="#">Packages</a>
                            </li>

                            <li class="nav-item">
                                <a class="nav-link active" href="#">Blog</a>
                            </li>

                            <li class="nav-item">
                                <a class="nav-link active" href="#">Contact</a>
                            </li>
                        </ul>
                    </div>
                </div>

                <div class="d-flex">
                    <div class="button-upcoming-events d-flex align-items-center"> 
                        <img src="../assets/img/helmet.png" alt="">  
                        <p>
                            Upcoming events
                        </p>
                        <i class="fa-solid fa-arrow-right"></i>
                    </div>
                </div>
            


            </div>
        </nav> 
    </header>

</template>

<style lang="scss" scoped>

header {
    background-color: white;
}

img {
    width: 220px;
}

.navbar {
    margin: 0 100px;
}

.navbar-expand-lg .offcanvas {
flex-grow: 0;
}

.nav-item {
    padding: 0 10px;
}

.button-upcoming-events {
    background-color: black;
    color: white;
    padding: 20px;
}

.button-upcoming-events img {
  filter: invert(100%);
  width: 50px;
}

.button-upcoming-events > * {
    margin: 0 5px;
}

p {
    margin-bottom: 0;
}




</style>
