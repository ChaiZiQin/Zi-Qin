# Zi Qin Portfolio <3
Year 3 NUS Economics student
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Lorem ipsum dolor</title>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.0/animate.min.css"
    />
    <link
      rel="stylesheet"
      href="https://use.fontawesome.com/releases/v5.7.1/css/all.css"
      integrity="sha384-fnmOCqbTlWIlj8LyTjo7mOUStjsKC4pOpQbqyi7RrhN7udi9RwhKkMHpvLbHG9Sr"
      crossorigin="anonymous"
    />
    <script
      src="https://code.jquery.com/jquery-3.4.1.min.js"
      integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo="
      crossorigin="anonymous"
    ></script>
  </head>
  <body>
    <div id="loading">
      <div id="spinner"></div>
    </div>
    <a href="/" class="go_back"><i class="fas fa-arrow-left"></i></a>
    <div id="background_overlay"></div>
    <div id="background"></div>
    <table id="profile_blog">
      <tbody>
        <tr>
          <td style="width:8vw;"><div id="profile_img_blog"></div></td>
          <td style="width:52vw;">
            <div id="username_blog"></div>
          </td>
        </tr>
      </tbody>
    </table>
    <div id="blog-display">
      <h1 id="blog_title">Lorem ipsum dolor</h1>
      <h2 id="blog_sub_title">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      </h2>
      <div id="blog">
        <img
          src="https://images.unsplash.com/photo-1553748024-d1b27fb3f960?w=1450"
        />
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut placerat
          pretium sem, ac maximus dui sodales a. Nunc aliquet hendrerit turpis
          ac egestas. Phasellus volutpat tristique maximus.
          <b>Pellentesque feugiat eget nisi et dignissim.</b> Nam nibh erat,
          sollicitudin non facilisis nec, scelerisque nec ipsum. Sed accumsan
          velit condimentum, pharetra felis vitae, commodo tellus.
          <u><i>Mauris consequat luctus orci.</i></u>
        </p>
        <p>
          Vivamus pharetra lobortis dui non tincidunt. Mauris vitae nisi
          vestibulum, mollis magna a, maximus mi. Suspendisse dictum eget augue
          quis sodales. Quisque rutrum ligula nec dapibus tincidunt.
          <span
            >Proin hendrerit massa a tellus vestibulum, a hendrerit ipsum
            iaculis. Suspendisse potenti.</span
          >
          Praesent eget erat blandit, finibus sapien vitae, ullamcorper erat.
          Integer blandit, felis at ullamcorper maximus, odio lectus pretium
          mauris, vel consequat lectus quam eu risus. Pellentesque gravida nec
          diam eget vehicula.
        </p>
        <img
          src="https://images.unsplash.com/photo-1556814278-8906c7d3a05f?w=1050"
        />
        <p>
          Donec hendrerit turpis non libero eleifend dignissim. Mauris non
          tempor metus, et tristique massa. Integer consequat justo quam, vitae
          aliquam arcu vestibulum at. Donec porttitor quam in tempus convallis.
          Praesent feugiat eget eros vitae accumsan. Duis ultricies odio quis
          nisl volutpat, consectetur imperdiet sem laoreet. Quisque maximus
          semper ligula at tincidunt. Pellentesque accumsan varius vehicula.
        </p>
      </div>
    </div>
    <div id="footer_blog">
      <a href="https://github.com/imfunniee" target="_blank"
        >made on earth by a human</a
      >
    </div>
    <script type="text/javascript">
      setTimeout(function() {
        document.getElementById("loading").classList.add("animated");
        document.getElementById("loading").classList.add("fadeOut");
        setTimeout(function() {
          document.getElementById("loading").classList.remove("animated");
          document.getElementById("loading").classList.remove("fadeOut");
          document.getElementById("loading").style.display = "none";
        }, 800);
      }, 1500);
      $.getJSON("../../config.json", function(user) {
        var icon = document.createElement("link");
        icon.setAttribute("rel", "icon");
        icon.setAttribute("href", user[0].userimg);
        icon.setAttribute("type", "image/png");
        document.getElementsByTagName("head")[0].appendChild(icon);
        document.getElementById(
          "profile_img_blog"
        ).style.background = `url('${user[0].userimg}') center center`;
        document.getElementById(
          "username_blog"
        ).innerHTML = `<span style="display:${
          user[0].name == null || !user[0].name ? "none" : "block"
        };">${user[0].name}</span>@${user[0].username}<b id="blog_time"></b>`;

        if ((user[0].theme = "dark.css")) {
          document.querySelector("#background_overlay").style.background =
            "linear-gradient(0deg, rgba(10, 10, 10, 1), rgba(10, 10, 10, 0.1))";
        } else {
          document.querySelector("#background_overlay").style.background =
            "linear-gradient(0deg, rgba(255, 255, 255, 1), rgba(255, 255, 255, 0.1))";
        }
      });
    </script>
  </body>
</html>
