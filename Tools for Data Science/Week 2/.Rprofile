.First <- function(){
  if(interactive()){
    cat("###########################################################################################\n")
    cat("\n")
    cat("Welcome to RStudio IDE!\n")
    cat("\n")
    cat("1. Your working directory is set to '/resources/rstudio'. We recommend you to use \n")
    cat("'resources/data' to store your data that will be available to other Data Scientist Workbench \n")
    cat("components, such as Jupyter Notebook.\n")
    cat("\n")
    cat("2. SparkR run-time environment is initialized. The 'sc' SparkContext is already defined \n")
    cat("for you to run Apache Spark from R.\n")
    cat("###########################################################################################\n")
    cat("\n")

    options(repos=structure(c(CRAN="http://cran.utstat.utoronto.ca/")))
    Sys.setenv('SPARKR_SUBMIT_ARGS'='"--packages" "com.databricks:spark-csv_2.11:1.4.0" "sparkr-shell"')
    .libPaths(c(.libPaths(), file.path(Sys.getenv("SPARK_HOME"), "R", "lib")))
    library(SparkR)

    # Changed from sparkR.session()
    sc <<- sparkR.session()

    setwd("/resources/rstudio/")
  }
}
