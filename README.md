# Liferay :: Hook for Servlet Filter throws Exception after server restart on WildFly

This repository has the purpose of being a support to resolve the problem reported in the following forum thread:
https://web.liferay.com/es/community/forums/-/message_boards/message/110177652

Steps to reproduce the error:

1. Download [WildFly 10.1.0.Final zip](http://download.jboss.org/wildfly/10.1.0.Final/wildfly-10.1.0.Final.zip)
2. Create the directory _C:\liferay-portal-6.2.5_ and then unzip the server there.
3. Merge the files of folder _wildfly-10.1.0.Final_ of this repo. This will prepare the server for Liferay deploy, based of the aplicable steps of this guides: [INSTALLING LIFERAY ON JBOSS 7.1](https://dev.liferay.com/es/discover/deployment/-/knowledge_base/6-2/installing-liferay-on-jboss-7-1) and [INSTALLING LIFERAY PORTAL ON WILDFLY 10](https://dev.liferay.com/es/discover/deployment/-/knowledge_base/7-0/installing-liferay-on-wildfly-10)
4. Download [liferay war](https://sourceforge.net/projects/lportal/files/Liferay%20Portal/6.2.5%20GA6/liferay-portal-6.2-ce-ga6-20160112152609836.war/download) and unzip in the directory _C:\liferay-portal-6.2.5\wildfly-10.1.0.Final\standalone\deployments\ROOT.war_
5. Start and initialize server
6. Compile _sample-servlet-filter-hook_ of this repo, it is a maven adaptation of the [liferay hook sample](https://github.com/liferay/liferay-plugins/tree/6.2.x/hooks/sample-servlet-filter-hook) then install it from control panel or C:\liferay-portal-6.2.5\deploy folder.
7. Restart server
