<template>
  <div>
    <table class="table">
      <thead>
      <tr>
        <th scope="col">순번</th>
        <th scope="col">제목</th>
        <th scope="col">작성자</th>
        <th scope="col">작성일</th>
        <th scope="col">조회수</th>
      </tr>
      </thead>
      <tbody>
      <tr>
        <th scope="row">{{ 게시판[0].number }}</th>
        <td>{{ 게시판[0].title }}</td>
        <td>{{ 게시판[0].name }}</td>
        <td>{{ 게시판[0].date }}</td>
        <td>{{ 게시판[0].view }}</td>
      </tr>
      <tr>
        <th scope="row">2</th>
        <td>{{ 게시판[1].title }}</td>
        <td>Thornton</td>
        <td>@fat</td>
        <td>@mdo</td>
      </tr>
      <tr>
        <th scope="row">3</th>
        <td>{{ 게시판[2].title }}</td>
        <td>@mdo</td>
        <td>@twitter</td>
        <td>@mdo</td>
      </tr>
      <tr>
        <th scope="row">4</th>
        <td>{{ 게시판[3].title }}</td>
        <td>@mdo</td>
        <td>@twitter</td>
        <td>@mdo</td>
      </tr>
      <tr>
        <th scope="row">5</th>
        <td>{{ 게시판[4].title }}</td>
        <td>Otto</td>
        <td>@mdo</td>
        <td>@mdo</td>
      </tr>
      <tr>
        <th scope="row">6</th>
        <td>{{ 게시판[5].title }}</td>
        <td>Otto</td>
        <td>@mdo</td>
        <td>@mdo</td>
      </tr>
      <tr>
        <th scope="row">7</th>
        <td>{{ 게시판[6].title }}</td>
        <td>Otto</td>
        <td>@mdo</td>
        <td>@mdo</td>
      </tr>
      </tbody>
    </table>
  </div>
</template>
<script>
export default {
  name : 'list',
  props : {
    게시판 : Array,
  }
}
</script>
<style>

</style>