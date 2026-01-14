<!--
author:   Alexander Botzki
email:    alexander.botzki@vib.be
version:  0.0.2
language: en
icon:     https://vib.be/sites/vib.sites.vib.be/files/logo_VIB_noTagline.svg
narrator: US English Female
comment:  This document provides a collection of LiaScript macros for the VIB material template.

@JSONLD
<script run-once>
  let json = @0 

  const script = document.createElement('script');
  script.type = 'application/ld+json';
  script.text = JSON.stringify(json);

  document.head.appendChild(script);

  // this is only needed to prevent and output,
  // as long as the result of a script is undefined,
  // it is not shown or rendered within LiaScript
  console.debug("added json to head")
</script>
@end


@orcid: [@0](@1)<!--class="orcid-logo-for-author-list"-->

-->


# Macros

          --{{0}}--
Macro for VIB training material

__Try it on LiaScript:__

https://liascript.github.io/course/?https://raw.githubusercontent.com/vib-tcp/training_material_template/new/main/macro.md
