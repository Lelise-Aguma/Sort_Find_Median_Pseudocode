// Pseudocode
FUNCTION sortAndFindMedian(numbers)
    CALL sort(numbers)

    DEFINE n = LENGTH(numbers)
    IF (n MOD 2 = 0) THEN
        // Even number of elements
        RETURN (numbers[n/2 - 1] + numbers[n/2]) / 2
    ELSE
        // Odd number of elements
        RETURN numbers[n/2]
    ENDIF
ENDFUNCTION

FUNCTION sort(numbers)
    DEFINE n = LENGTH(numbers)
    FOR i = 0 TO n-1
        FOR j = 0 TO n - i - 2
            IF numbers[j] > numbers[j+1] THEN
                // Swap numbers[j] and numbers[j+1]
                temp = numbers[j]
                numbers[j] = numbers[j+1]
                numbers[j+1] = temp
            ENDIF
        ENDFOR
    ENDFOR
ENDFUNCTION
