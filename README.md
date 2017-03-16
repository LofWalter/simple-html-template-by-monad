# simple-html-template-by-monad
# simple-html-template-by-monad


this project is just a funny thought ,including monad thought , developer can compile the html template without dependencies easily.


let viewContainer = function (module,arg) {
      this.module = module
      this.arg = arg
  }

  viewContainer.of = function (module,arg) {
      return new viewContainer(module,arg)
  }

  viewContainer.prototype.map = function (target) {
      document.getElementById(target).innerHTML =  this.module(this.arg)
  }


viewContainer.of(mf,arg)   -->    .map(target)

template  -->   Dom


developer can extend the function of viewContainer  and realize more  
