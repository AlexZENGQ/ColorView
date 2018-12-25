## Bootstrap框架
Bootstrap，来自 Twitter，是目前最受欢迎的前端框架。Bootstrap 是基于 HTML、CSS、JAVASCRIPT 的，它简洁灵活，使得 Web 开发更加快捷。由 Twitter 的 Mark Otto 和 Jacob Thornton 开发。 2011 年八月在 GitHub 上发布的开源产品。

官方文档：https://getbootstrap.com/docs/4.1/getting-started/introduction/

### 首先是进入 Bootstrap Documentation 导入 依赖的文件包 Starter template
```
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">

    <title>Hello, world!</title>
  </head>
  <body>
    <!-- Optional JavaScript -->
    <!-- jQuery first, then Popper.js, then Bootstrap JS -->
    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>
  </body>
</html>
```

### 接着在以上的代码中 “<body>” 下开始写入代码
  >>记得 Bootstrap 整体是包含在 <div class="comtanier>...</div>之中 ，并使用已有组件进行创建
    
    1.标题以及三张图连续展示，Gird网格系统，bootstrap运用的是12格网格，可以随意分成一份、两份、三份、四份
    <div class="row">
        <div class="col-md-6"><img class="title-logo" src="images/title1.png" height="100" alt="AlexZENGQlogo"></div>
        <div class="col-md-6 text-uppercase text-right">
          <h1 style="letter-spacing: 4px;" class="title-super text-thin">AlexZENG·Q</h1>
          <h5>From Nanning</h5>
        </div>
      </div>
      <hr/>
      <div class="row">
        <div class="col-md-12">
          <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
            <ol class="carousel-indicators">
              <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
              <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
              <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
            </ol>
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img src="images/m1.png" class="d-block w-100" alt="#">
              </div>
              <div class="carousel-item">
                <img src="images/m1-2.png" class="d-block w-100" alt="#">
              </div>
              <div class="carousel-item">
                <img src="images/m1-3.png" class="d-block w-100" alt="#">
              </div>
            </div>
            <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
              <span class="sr-only">Previous</span>
            </a>
            <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
              <span class="sr-only">Next</span>
            </a>
          </div>
        </div>  
      </div>
      
      
      
      
      2.四张图的展示，并使用 Modal 响应式弹出
      
      <div class="row" style="height: 20px;"></div>
      <div class="row">
        <div class="col-md-12">
          <h2 class="text-muted">Color View</h2>
        </div> 
      </div>
      <div class="row text-center">
        <div class="col-md-6">
          <img src="images/m2.png" class="img-fluid" alt="color2" data-toggle="modal" data-target="#project2">
          <h3 class="text-uppercase">ONE</h3>
          <P>https://github.com/AlexZENGQ</P>
        </div>
        <div class="col-md-6">
          <img src="images/m3.png" class="img-fluid" alt="color3" data-toggle="modal" data-target="#project3">
          <h3 class="text-uppercase">two</h3>
          <P>https://github.com/AlexZENGQ</P>
        </div>
      </div>
      <div class="row text-center">
        <div class="col-md-6">
          <img src="images/m4.png" class="img-fluid" alt="color4" data-toggle="modal" data-target="#project4">
          <h3 class="text-uppercase">three</h3>
          <P>https://github.com/AlexZENGQ</P>
        </div>
        <div class="col-md-6">
          <img src="images/m5.png" class="img-fluid" alt="color5" data-toggle="modal" data-target="#project5">
          <h3 class="text-uppercase">four</h3>
          <P>https://github.com/AlexZENGQ</P>
        </div>
      </div>
    </div>

    <!-- Modal -->
    <div class="modal fade" id="project2" tabindex="-1" role="dialog" aria-labelledby="topleft1" aria-hidden="true">
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="topleft1">ONE</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <img src="images/m2.png" class="img-fluid">
            Green is the color between blue and yellow on the visible spectrum. It is evoked by light which has a dominant wavelength of roughly 495–570 nm. 
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
          </div>
        </div>
      </div>
    </div>

    <div class="modal fade" id="project3" tabindex="-1" role="dialog" aria-labelledby="topright1" aria-hidden="true">
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="topleft2">TWO</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <img src="images/m3.png" class="img-fluid">
            Purple is a color intermediate between blue and red.It is similar to violet, but unlike violet, which is a spectral color with its own wavelength on the visible spectrum of light, purple is a composite color made by combining red and blue.
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
          </div>
        </div>
      </div>
    </div>

    <div class="modal fade" id="project4" tabindex="-1" role="dialog" aria-labelledby="buttonleft1" aria-hidden="true">
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="buttonleft1">THREE</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <img src="images/m4.png" class="img-fluid">
            Blue is one of the three primary colours of pigments in painting and traditional colour theory, as well as in the RGB colour model.
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
          </div>
        </div>
      </div>
    </div>

    <div class="modal fade" id="project5" tabindex="-1" role="dialog" aria-labelledby="buttonright1" aria-hidden="true">
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="buttonright1">FOUR</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <img src="images/m5.png" class="img-fluid">
            Teal is a medium blue-green color, similar to cyan. Its name comes from that of a bird—the common teal (Anas crecca)—which presents a similarly colored stripe on its head. 
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
          </div>
        </div>
      </div>
    </div>
    
    
    
    3.最后根据自己的设计想法或者已有图纸，设计出不同的css满足要求

