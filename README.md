# displaytag-1.2
Custom displaytag-1.2.jar: sortable column links "rel=nofollow"

Original source code:
http://svn.code.sf.net/p/displaytag/code/tags/displaytag-doc-1.2

Updates:

- removed from original project:
displaytag-examples/
displaytag-export-poi/
displaytag-portlet/

- displaytag/pom.xml:
      <plugin>
        <artifactId>maven-surefire-plugin</artifactId>
        <version>2.17</version>
        <configuration>
    		<skipTests>true</skipTests>
  		</configuration>
        <!--
        <configuration>
          <includes>
            <include>**/TestAll.java</include>
          </includes>
        </configuration>
        -->
      </plugin>
      
- org.displaytag.render.HtmlTableWriter:
Line 468:
  header = header.replaceFirst("<a", "<a rel=\"nofollow\"");
