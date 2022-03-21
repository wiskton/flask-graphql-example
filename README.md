# flask-graphql-example


Running project

    poetry initCancel changes
    poetry add flask ariadne flask-sqlalchemy flask-cors
    poetry shell
    flask run


Open the browser

    http://localhost:5000/graphql


Example show posts:

    query AllPosts {
      listPosts {
        success
        errors
        post {
          id
          title 
          description
          created_at
        }
      }
    }


Example create post:

    mutation CreateNewPost {
      createPost(
        title: "New Blog Post", 
        description:"Some Description") {
        post {
          id
          title
          description
          created_at
        }
        success
        errors
      }
    }


Example show post:

    query GetPost {
      getPost(id: "1") {
        post {
          id
          title
          description
        }
        success
        errors
      }
    }


Example update post:

    mutation UpdatePost {
      updatePost(id:"2", title:"Hello title", description:"updated description") {
        post {
          id
          title
          description
        }
        success
        errors
      }
    }


Example delete post:

    mutation DeletePost {
      deletePost(id:"1") {
        success
        errors
      }
    }
