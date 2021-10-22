# matrix
Implementation of Matrix and Vector Objects in Crystal

## Progress
* Matrix class initiated
* row and col functionality implemented

## todo
* decide whether to use struct or class
* Matrix.diagonal(9, 5, -3)
* Matrix.scalar(dim=2, entries=5)
* Matrix.zero(row_count, column_count = row_count)
* Matrix.vstack(x, *matrices)
* Matrix.hstack(x, *matrices)
* Matrix.combine(*matrices) { |*elements| ... }
  * x = Matrix[[6, 6], [4, 4]]
  * y = Matrix[[1, 2], [3, 4]]
  * Matrix.combine(x, y) {|a, b| a - b} # => Matrix[[5, 4], [1, 0]]
* initialization of matrix with empty rows and cols
* fill matrix with zeros (or else)
* collect(which = :all, &block)
  * use case
  * :all (default): yields all elements
  * :diagonal: yields only elements on the diagonal
  * :off_diagonal: yields all elements except on the diagonal
  * :lower: yields only elements on or below the diagonal
  * :strict_lower: yields only elements below the diagonal
  * :strict_upper: yields only elements above the diagonal
  * :upper: yields only elements on or above the diagonal
  * Matrix[ [1,2], [3,4] ].collect { |e| e**2 }
    * __1 _4
    * __9 16
* Matrix.each :byrow, :bycol, :all etc similar to collect
  * use case
* get value by row and col-index
* Error handling (raise)
* Tests:
  * symmetric?
  * diagonal?
  * square?
  * empty?
  * has_na?
  * has_zero?
  * is_identity?
  * is_lower?
  * is_upper?
  * hermitian?
  * normal?
* == for Vector and Matrix
* mult(*) for Vector and Matrix
* division (/) (multiplication by the inverse) for Vector and Matrix
  * Matrix[[7,6], [3,9]] / Matrix[[2,9], [3,1]]
  * => -7 _1
  * ___ -3 -6
* add(+) for Vector and Matrix
* sub(-) for Vector and Matrix
