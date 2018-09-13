
<div class="modal fade" tabindex="-1" role="dialog" id="addNew" aria-labelledby="addNewlabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered" role="document">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="addNew">Add User  </h5>
                <button type="button" class="close" data-dismiss="modal" 
                aria-label="close">
                <span aria-hidden="true">&times;</span></button>
            </div>
            <div class="modal-body">
              <div class="form-group">
                  <input type="text" v-model="form.name" name="name" placeholder="Name"
                 class="form-control" :class="{'is-invalid':form.errors.has('name')}">
                <has-error :form="form" field="name"></has-error>
              </div>
              <div class="form-group">
                  <input type="email" v-model="form.email" name="email" placeholder="Email"
                 class="form-control" :class="{'is-invalid':form.errors.has('email')}">
                <has-error :form="form" field="email"></has-error>
              </div>

              <div class="form-group">
                  <textarea v-model="form.bio" name="bio" placeholder="Bio"
                 class="form-control" :class="{'is-invalid':form.errors.has('bio')}"> </textarea>
                <has-error :form="form" field="bio"></has-error>
              </div>
               <div class="form-group">
                  <select name="type" v-model="form.bio" id="type" class="form-control"
                  :class="{'is-invalid':form.errors.has('type')}">
                  <option value="Select User Role"></option>
                  <option value="Admin"></option>
                  <option value="User"></option>
                  <option value="Author"></option>
                  </select>
                <has-error :form="form" field="bio"></has-error>
              </div>
              <div class="form-group">
                  <input type="password" v-model="form.password" name="password" id="password" placeholder="Password"
                 class="form-control" :class="{'is-invalid':form.errors.has('password')}">
                <has-error :form="form" field="password"></has-error>
              </div>

            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-danger" data-dismiss="modal">Close </button>
                 <button type="button" class="btn btn-primary">Create</button>
                 
            </div>
        </div>

    </div>
</div>