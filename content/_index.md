---
title: "Home"
---

<!-- Redirect Netlify Identity invite/verify token to /admin -->
<script>
(function () {
  // token có thể nằm ở query (?invite_token=...) hoặc hash (#invite_token=...)
  var q = window.location.search || "";
  var h = window.location.hash || "";
  if (q.indexOf("invite_token=") !== -1) {
    window.location.replace("/admin/" + q);
  } else if (h.indexOf("invite_token=") !== -1) {
    window.location.replace("/admin/" + h);
  }
})();
</script>
