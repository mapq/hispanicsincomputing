---
layout: default
title: Hispanics in Computing
subtitle: Statement from Hispanics in Computing
banner: banner.jpg
anonymous: 1
signed:
  - name: Manuel A. Pérez-Quiñones
  - name: Ann Gates
  - name: Juan Sequeda
  - name: Adriana Alvarado Garcia
  - name: Wilson Lozano
  - name: Francisco Raul Ortega, Ph.D.
  - name: Brianna B. Posadas, Ph.D.
  - name: Jaime Ruiz, Ph.D.
  - name: Lucio Lopez
  - name: José R. Ortiz Ubarri
  - name: IAlfredo Cruz, Ph.D.
  - name: Hiram Moya, Ph.D.
  - name: Cecilia Aragon, Ph.D.
  - name: Rafael Arce Nazario
  - name: Rei Sanchez-Arias, Ph.D.
  - name: Rogelio E. Cardona-Rivera, Ph.D.
  - name: Patricia Lopez, Ph.D.
  - name: Raul Viera-Mercado
  - name: Andrés Monroy-Hernández, Ph.D.
  - name: Lizzet Clifton
  - name: Marisol Wong-Villacres
  - name: Eliana Valenzuela-Andrade, Ph.D
  - name: Dan Garcia, Ph.D.
  - name: Joslenne Peña, Ph.D.
  - name: Katya Borgos-Rodriguez
  - name: Christine Alvarado
  - name: Anamary Leal Ph.D
  - name: Raena Cota
  - name: Carlos J Corrada Bravo, Ph.D.
  - name: Bryan Y. Hernández Cuevas, Ph.D. Student
  - name: Maria De-Arteaga, Ph.D.
  - name: Jose Luis Manners
  - name: Edward Latorre-Navarro
  - name: Miguel Velez-Reyes, Ph.D., PE
  - name: Patricia Ordóñez, Ph.D.
  - name: Benjamin C. Flores, Ph.D.
  - name: Vanessa Frias-Martinez, Ph.D.
  - name: Alvaro Monge, Ph.D.
  - name: Victoria C. Chávez
  - name: Marco Alvarez

ally:
  - name: Odest Chadwicke Jenkins, Ph.D.
  - name: Sergio D Cabrera, Ph.D.
  - name: Bryant W York, Ph.D.
---

Throughout history, this country has struggled to accept different groups as equal partners in society. The recent protests caused by numerous attacks on members of the Black community serve as evidence that we still have work to do.

As members of the Hispanics in Computing, we would like to express our support for the Black community, including the Black Hispanic community, and echo their call to action and demand for justice (<https://blackincomputing.org/>). We must work hard to dismantle systemic discrimination that has hampered the pursuit for equality for many groups in our society. Today, while we focus our attention on injustices against Black people in the US, we also acknowledge other marginalized groups that face similar struggles for justice and equality. Recent court decisions on the protection of members of the LGBTQ+ community against employment discrimination, and the protection to DACA immigrants show that the march towards equality continues.

The undersigned are members of the Hispanics in Computing group and other allies. We are a group of computing professionals, faculty and students interested in the mentoring, promotion, and career advancement of Hispanics in computing.

\#BlackLivesMatter

{% assign public = 0%}

**Members of Hispanic in Computing**
<ul>
{% for person in page.signed %}
<li>{{person.name}}</li>
{% if forloop.last == true %}{% assign public = forloop.index %}{%endif%}
{% endfor %}
</ul>

**Allies of Hispanic in Computing**
<ul>
{% for person in page.ally %}
<li>{{person.name}}</li>
{% if forloop.last == true %}{% assign public = public | plus: forloop.index %}{%endif%}
{% endfor %}
</ul>

{% assign total = public | plus: page.anonymous %}
Total of {{total}} signatures, {{public}} shown publicly.

