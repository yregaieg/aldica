# Introduction

Fetch the newest amps:
* de.acosix.alfresco.utility.core.repo-1.{{ VERSION }}.amp
* aldica-repo-ignite-{{ VERSION }}.amp
* support-tools-repo-{{ VERSION }}.amp

Place these into a folder called `amps`, and add a `Dockerfile` with the following contents next to it:
```
FROM alfresco/alfresco-content-repository-community:{{ VERSION }}

ADD amps/de.acosix.alfresco.utility.core.repo-1.{{ VERSION }}.amp amps
RUN java -jar alfresco-mmt/alfresco-mmt-6.0.jar install amps/de.acosix.alfresco.utility.core.repo-1.{{ VERSION }}.amp webapps/alfresco

ADD amps/aldica-repo-ignite-{{ VERSION }}.amp amps
RUN java -jar alfresco-mmt/alfresco-mmt-6.0.jar install amps/aldica-repo-ignite-{{ VERSION }}.amp webapps/alfresco

ADD amps/support-tools-repo-{{ VERSION }}.amp amps
RUN java -jar alfresco-mmt/alfresco-mmt-6.0.jar install amps/support-tools-repo-{{ VERSION }}.amp webapps/alfresco

RUN rm -rf webapps/alfresco-*.bak
```
