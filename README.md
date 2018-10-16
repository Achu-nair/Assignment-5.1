# Assignment-5.1
Assignment for acadguild


      library(stringr)

      #calculate the number of vovwels in USA STATES.

      #names of states
      states = row.names(USArrests)
      states
      #vector vowels
      vowels = c("a","e","i","o","u")
      vowels

      #store the results

      numv = vector(mode = "integer",length = 5)

      #calculate the number of vowels
      for(j in seq_along(vowels))
      {
        numc = str_count(tolower(states),vowels[j])
        numv[j] = sum(numc)
      }
      names(numv) = vowels
      numv
      #sort vowels
      sort(numv, decreasing = TRUE)

      #create barplot 
      barplot(numv, main = "Number of vowels in USA States names",xlab = "vowels",
              ylab = "number",border = NA, ylim = c(0, 80),col = "orange")
