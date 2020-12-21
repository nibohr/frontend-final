<template>
    <div id="services" class="container SecServicios">
        <div>
            <h2 class="text-center font-weight-normal pl-5 mlr-5">Servicios</h2>
          </div>
    
          <div class="row justify-content-center">
            <div class="mt-5 pt-5 col-sm-6 ">
              <div class="card bg-light border border-primary shadow">
                <img src="../../public/img/cenefaMarketing.jpg" class="card-img-top" alt="imagen restaurante">
                <div class="card-body">
                  <h5 class="card-title text-dark">Marketing Digital</h5>
                  <p class="card-text text-dark">Aplicamos estrategias de comercialización llevadas a cabo en los medios digitales. Todas las técnicas del mundo off-line son imitadas y traducidas a un nuevo mundo, el mundo online.
                  </p>
                        <!-- Button trigger modal -->
                    <button type="button" class="btn btn-info text-white float-right" data-toggle="modal" data-target="#staticBackdrop">
                    VER PORTAFOLIO
                    </button>

                    <!-- Modal -->
                    <div class="modal fade" id="staticBackdrop" data-backdrop="static" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
                    <div class="modal-dialog modal-dialog-centered modal-dialog-scrollable">
                        <div class="modal-content">
                        <div class="modal-header bg-dark">
                            <h5 class="modal-title text-white" id="staticBackdrop">Portafolio de productos</h5>
                            <button type="button" class="close text-white" data-dismiss="modal" aria-label="Close">
                                <span aria-hidden="true">&times;</span>
                            </button>
                        </div>
                        <div class="modal-body">
                            <h5 class="text-info">Marketing Digital</h5>
                            <p>
                            <ul class="list-group list-group-flush p-0">
                                <li class="list-group-item">SEO y Posicionamiento Web</li>
                                <li class="list-group-item">Posicionamiento en redes</li>
                                <li class="list-group-item">Fotografía y Video</li>
                                <li class="list-group-item">Email Marketing</li>
                                <li class="list-group-item">Merchandising</li>
                            </ul>
                            </p>
                        </div>
                        <div class="modal-footer">
                            <button type="button" class="btn btn-info text-white" data-dismiss="modal">OK</button>
                        </div>
                        </div>
                    </div>
                    </div>
                </div>
              </div>
            </div>

          </div>
    </div>
</template>
<script>
export default {
    name: 'SecServicos'
}
</script>
<style scoped>
#services{
    padding-top: 80px !important;
}

h2{
    color: #00ACC1;
    text-align: left !important;
}

</style>