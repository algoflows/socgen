<script>
  import { Navbar } from "shared/ui";
  import "../app.css";

  const logoUrl =
    "/src/assets/soc-gen-high-resolution-logo-color-on-transparent-background.png";

  const links = [
    { label: "Home", href: "/" },
    { label: "Features", href: "/features" },
    { label: "Pricing", href: "/pricing" },
    { label: "Learn", href: "/learn" },
    { label: "About", href: "/about" },
    { label: "Signin", href: "/auth" },
  ];
</script>

<div class="max-w-4xl min-h-screen px-4 py-4 m-auto border max-md:px-6">
  <!-- Navbar -->
  <div class="mb-6 border">
    <Navbar {links} imgUrl={logoUrl} />
  </div>
  <!-- Slot -->
  <div class="max-w-full min-h-screen border">
    <slot />
  </div>
</div>
