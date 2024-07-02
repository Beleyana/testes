Commit changes<div class="container my-5"> 
  <center><h1>Поиск </h1></center> <br>
  <form method="POST" action="" class="mb-5">
    <div class="row">
      <div class="col-md-4">
        <select name="searchType" class="form-select" required>
          <option value="">Вид</option>
          <option value="attrakcion" <?php if ($searchType 'attrakcion') echo 'selected'; ?>>Аттракционы</option>
        </select>
  </div>
  <div class="col-md-6">
  <input type="text" name="searchQuery" class="form-control" placeholder=" название" value="<?php echo htmlspecialchars($searchQuery); ?>" require>
  </div>
  <div class="col-md-2">
  <button type="submit" class="btn btn-primary w-100">Поиск</button>
  </div>
  </div>
  </form>

  <?php if (!empty($searchResults)): ?>
    <div class="row">

  <?php foreach ($searchResults as $result): ?>
    <div class="col-md-3 mb-4"> 
      <div class="card h-100">
        <img src="png/<?php echo htmlspecialchars($result['src']); ?>.png" class="card-img-top" alt="<?php echo htmlspecialchars($result['title']); ?>"
        <div class="card-body">
        <h5 class="card-title"><?php echo htmlspecialchars(Sresult['name']); ?></h5>
        <p class="card-text"><?php echo htmlspecialchars(Sresult['vid']);?></p>
      </div>
    </div>
  </div>

  <?php endforeach; ?>
  </div>
  <?php elseif ($_SERVER['REQUEST_METHOD'] == "POST"): ?>
    <div class-"alert alert-warning" role-"alert">
         Ничего не найдено 
      </div>
  <?php endif; ?>
  </diy>
