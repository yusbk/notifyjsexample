#' @import shiny
app_ui <- function() {
  tagList(
    # Leave this function for adding external resources
    golem_add_external_resources(),
    # List the first level UI elements here 
    fluidPage(
      h1("Notifyjs in Shiny Example"), 
      mod_my_first_module_ui("my_first_module_ui_1"), 
      mod_my_second_module_ui("my_second_module_ui_1")
    )
  )
}

#' @import shiny
golem_add_external_resources <- function(){
  
  addResourcePath(
    'www', system.file('app/www', package = 'notifyjsexample')
  )
 
  tags$head(
    golem::activate_js(),
    golem::favicon(),
    # Add here all the external resources
    # If you have a custom.css in the inst/app/www
    # Or for example, you can add shinyalert::useShinyalert() here
    htmltools::htmlDependency(
      "notifyjs", version = "0.1.0", 
      src = system.file('app/www', package = 'notifyjsexample'), 
      script = "notify.js"
    ), 
    tags$script(src="www/handlers.js"), 
    tags$link(rel="stylesheet", type="text/css", href="www/custom.css")
  )
}
