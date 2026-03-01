<header>
  <h1>
    <small>Assignment 3</small>
    Visualization Critique & Redesign
  </h1>

  <p>
    <strong>Wendy Zhang</strong> — <em>wendyz@mit.edu</em>
  </p>
</header>

<main>
  <section>
    <h2>Reading & Critique</h2>

    <figure>
      <img
        src="https://vis-society.github.io/assets/imgs/covid-spiral.png"
        alt=""
      />
    </figure>

    <p>Insights about the data/visualization:</p>

    <ul>
      <li>There is a drastic increase in January 2022</li>
      <li>
        It looks pretty consistent throughout 2021, except for a significant
        decrease between May to June
      </li>
      <li>There’s a pretty big increase in 2020 November to 2021 Feburary</li>
      <li>For most of the years, it stayed below around 200k</li>
      <li>The cases didn’t start until like middle of March of 2020</li>
    </ul>

    <p>Design Critique:</p>

    <p>
      I think they did a good job showing over two years of data in one compact
      chart. There is actually a lot of data shown, and if we were to unroll the
      spiral into a horizontal x-axis, it would be way too wide. I also think
      they do a good job making it easier to compare times where there are
      significantly more cases, since matching months over the years are above
      each other, and connecting months are next to each other. The spacing and
      labels (like “7-day average”) also leave good room to breathe and make the
      chart more approachable. I think it does a good job of expressing to the
      target audience when cases have gone up and how drastic January 2022 was
      due to the new Omicron variant.
      <br />
      I think one small improvement would be to add more text to caption parts of
      the graph that they want to stand out. I also don’t know if I like the idea
      of the spiral going from a small to a big circle, since it makes it harder
      for people to judge the amount of new COVID cases intuitively just based on
      the volume. Instead, they have to look carefully at the heights. For example,
      while November 2020 to December 2020 is more serious than Nov 2021 to Dec 2021
      with more cases, the volume of the red area looks almost similar and makes
      them seem similarly bad. Another thing is that instead of measuring the height
      from the center line, they could provide a more straightforward frame of reference
      by maybe having the height start directly from the central spiral line. After
      reading the article, I also realized that the data after January 2022 are predictions
      and not real values. While seeing this graph in January 2022 might make that
      more intuitive, I feel like it would be better to clearly label those sections
      for people viewing it later so they know the data are projections. It’s also
      a bit confusing that the key doesn’t go up to the maximum width of some of
      the lines, after it goes beyond 150k cases, people have to estimate the values
      of some heights, especially in January 2021.
    </p>
  </section>

  <section>
    <h2>Visualization Sketches</h2>

    <figure>
      <img src="../../images/assn3_graphs/sketch1.png" alt="" />
      <figcaption>New Covid-19 cases bar graph</figcaption>
    </figure>

    <p>Design Rationale for Sketch 1:</p>

    <ul>
      <li>
        Motivation: I want to explore combining the data from different years
        but the same months to see if we can see trends in which months might
        have more cases.
      </li>
      <li>
        Goal: This way, we can see monthly trends and be able to predict in the
        future if a bad month is coming up and how we can better prepare for it.
      </li>
      <li>
        Work well: I like how it directly combines the years. We can see even
        more clearly how the cases differ between months. It also has clear
        labels for the heights or the number of cases instead of having to
        estimate based on a legend.
      </li>
      <li>
        Didn’t work well: It’s harder to see the trend between years (like from
        Dec of 2020 to Jan of 2021) compared to the spiral approach.
      </li>
      <li>
        Future exploration: I wonder if I can move away from the month on the
        x-axis and cases on the y-axis. Maybe there’s other things that can be
        seen without
      </li>
    </ul>

    <figure>
      <img src="../../images/assn3_graphs/sketch2.png" alt="" />
      <figcaption>New Covid-19 cases circle graph</figcaption>
    </figure>

    <p>Design Rationale for Sketch 2:</p>

    <ul>
      <li>
        Motivation: I wanted to try a different visualization form and look
        beyond temporal trends.
      </li>
      <li>
        Goal: By keeping each year in a section, we can clearly see which years
        have more cases. Keeping every month in one bubble, we can also clearly
        see which months have the most cases
      </li>
      <li>
        Work well: This way, we can see the main pressure points from the past
        years. Which months have the worst cases and people can maybe do an
        analysis based on that.
      </li>
      <li>
        Didn’t work well: We lose the ability to look for temporal trends and
        directly compare years or months to each other. The color is also kind
        of clustered and makes it hard to easily read. It doesn’t has clear
        labels for the number of cases in each circle and requires an estimate
        based on a legend.
      </li>
      <li>
        Future exploration: I want to keep exploring the temporal trends and see
        how cases change compared to neighboring months. I think this is better
        for planning for the future rather than just observing the past.
      </li>
    </ul>

    <figure>
      <img src="../../images/assn3_graphs/sketch3.png" alt="" />
      <figcaption>New Covid-19 cases line graph</figcaption>
    </figure>

    <p>Design Rationale for Sketch 3:</p>

    <ul>
      <li>
        Motivation: I like the idea of keeping the same months from different
        years next to each other to make it easier to compare general trends
        over the year. Since, as they mentioned in the article, there might be
        increases or similar trends over the holiday seasons (Nov to Feb or Jun
        to Aug) due to traveling or trends in case reporting.
      </li>
      <li>
        Goal: I wanted this line graph to communicate all the trends that are
        similar and different in the number of cases over the years. By having
        all the lines on top of each other, we can see similar increase or
        decrease in different months. We can also see how drastic the number of
        cases are in August of one year verses the next year.
      </li>
      <li>
        Work well: I think having the years stacked on each other makes it easy
        to quickly compare the same months over different years. It also keeps
        it very concise instead of having 36 months in the x-axis. It also has a
        common reference point starting at the x axis instead of being centered
        around an axis. It also has clear labels for the heights or the number
        of cases instead of having to estimate based on a legend.
      </li>
      <li>
        Didn’t work well: It’s harder to see the trend between years (like from
        Dec of 2020 to Jan of 2021) compared to the spiral approach.
      </li>
      <li>
        Future exploration: I wonder if I can edit the x-axis instead of pure
        value and try log instead to make sure no drastic values make the graph
        harder to read.
      </li>
    </ul>
  </section>

  <section>
    <h2>Final Visualization Design</h2>

    <figure>
      <img src="../../images/assn3_graphs/final.png" alt="" />
      <figcaption>New Covid-19 Cases Line Graph (2020 - 2022)</figcaption>
    </figure>
  </section>

  <section>
    <h2>Final Writeup</h2>

    <p>
      For my final design, I wanted to communicate all the trends that are
      similar and different in the number of cases over the 3 years. By having
      all the lines on top of each other on a month-by-month x-axis, we can
      clearly see similar increases or decreases in the same months over
      different years. We can more easily see how drastic the number of cases
      was in August 2020 compared to August 2021. My goal is to show monthly
      patterns and big spikes over the years. For the colors of the years, I
      decided to go from green, yellow, to red, to kind of represent the
      increasing risk or severity over the years. In 2020, the situation was
      still not as bad (in comparison to future years), while in 2022, cases
      spiked a lot with all the new variants. I chose a linear scale instead of
      a log scale because even though January 2022 is very high, most values
      were in a fairly small range between 0 and 6 million. Using a linear scale
      allows people to more clearly see month-to-month differences without
      squashing most of the data. I also rotated the x-axis labels and shortened
      them to three-letter abbreviations so people do not have to tilt their
      heads (as mentioned in lecture) to read them. Labeling the y-axis in 2M
      intervals felt like a good balance between precision and clarity to avoid
      clutter while not making people have to estimate too much.
    </p>

    <p>
      I think “critique by redesign” did a great job in making me better
      understand what I value in a visualization. I liked how the original had
      the same months aligned above each other, so I kept that in my design.
      However, I found that having the heights centered around an axis made it
      harder to compare the magnitudes, so I moved everything to a common
      reference point from the x-axis to provide a clearer reference point. I
      also made sure to include axis labels rather than relying on a legend for
      scale interpretation. For tradeoffs, it is now harder to see the
      continuous flow from December of one year to January of the next, and I
      appreciated that about the spiral approach. In general, the redesign
      process helped me a lot in being more international with my design choices
      and what I valued versus what I was willing to trade off.
    </p>
  </section>
</main>
