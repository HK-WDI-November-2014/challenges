# CSS Challenges

### Challenge 1

Write an HTML code that corresponds to the following CSS Selectors, and highlight the element(s) that would targeted but that selector. For example, ```p.main-text``` would render:

    <p class="main-text">
    </p>


* ``` div.hello.world ```
* ``` #restaurant-info > div.main-info  ```
* ``` article.article ```
* ``` ul > li ```
* ``` ul > li .highlight ```
* ``` ul > li:nth-child(3) ```
* ``` table.table > head > tr > td.name.first-name ```
* ``` .btn-group > .btn:first-child:not(:last-child) ```


### Challenge 2

Consider the following HTML code:

       <section>
          <header>
            <div>Section Title</div>
          </header>
          <div>
            <p>Sub title</p>
            <div>
              <div>1</div>
              <div>2</div>
              <div>3</div>
              <div>
                <div>4</div>
              </div>
            </div>
            <div>
              <div>11</div>
              <div>12</div>
              <div>13</div>
              <div>
                <div>14</div>
              </div>
            </div>
          </div>
        </section>

Using CSS Selectors, how would you change the text color of:

* Sub title
* Section Title
* All numbers
* Only 1,2,3 and 11,12,13
* Only 4 and 14
* Only 14
* Only 2
* 2 and 12
* 3 and 13


### Challenge 3

Using CSS, how would you add a grey background to every even row of that table (rows 2, 4, 6...):

        <table>
          <thead>
            <tr>
              <th></th>
              <th></th>
              <th></th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td></td>
              <td></td>
              <td></td>
            </tr>
            <tr><!-- this row should be grey --></tr>
            <tr>...</tr>
            <tr><!-- this row should be grey --></tr>
          </tbody>
        </table>
